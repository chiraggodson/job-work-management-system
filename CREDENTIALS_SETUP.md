# Google Sheets Credentials Setup Guide

## Step 1: Create Service Account

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Select your project
3. Go to "IAM & Admin" > "Service Accounts"
4. Click "Create Service Account"
5. Fill in the details:
   - Name: `job-work-sheets`
   - Description: `Service account for Job Work Orders app`
   - Click "Create and Continue"
6. Grant roles:
   - Role: "Editor" for Google Sheets API
   - Click "Continue"
7. Click "Done"

## Step 2: Generate Credentials

1. Find your service account in the list
2. Click on the email address
3. Go to "Keys" tab
4. Click "Add Key" > "Create new key"
5. Choose "JSON" format
6. Click "Create"
7. The JSON file will download automatically

## Step 3: Update credentials.json

1. Open the downloaded JSON file
2. Update `src/lib/credentials.json` with the following fields:
   ```json
   {
     "type": "service_account",
     "project_id": "your-project-id",
     "private_key_id": "your-private-key-id",
     "private_key": "your-private-key",
     "client_email": "your-service-account-email",
     "client_id": "your-client-id",
     "auth_uri": "https://accounts.google.com/o/oauth2/auth",
     "token_uri": "https://oauth2.googleapis.com/token",
     "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
     "client_x509_cert_url": "your-cert-url"
   }
   ```

   Replace these values:
   - `your-project-id`: Your Google Cloud project ID
   - `your-private-key-id`: The private key ID from the downloaded JSON
   - `your-private-key`: The private key from the downloaded JSON
   - `your-service-account-email`: The service account email address
   - `your-client-id`: The client ID from the downloaded JSON
   - `your-cert-url`: The client x509 cert URL from the downloaded JSON

## Step 4: Share Google Sheet

1. Open your Google Sheet
2. Click "Share" button
3. Add the service account email (found in `client_email` field)
4. Set permission to "Editor"
5. Uncheck "Notify people"
6. Click "Share"

## Important Security Notes

1. Never commit `credentials.json` to version control
2. Keep your private key secure
3. Restrict service account permissions to only what's needed
4. Regularly rotate service account keys
5. Monitor API usage in Google Cloud Console

## Troubleshooting

If you get authentication errors:
1. Verify all fields in credentials.json match the downloaded JSON
2. Ensure the Google Sheet is shared with the service account email
3. Check that the Google Sheets API is enabled
4. Verify the service account has the correct permissions
5. Check API quotas in Google Cloud Console

## Environment Variables

Remember to also set up your environment variables in `.env.local`:
```env
NEXT_PUBLIC_GOOGLE_SHEETS_ID=your_spreadsheet_id
```

The spreadsheet ID can be found in your Google Sheet URL:
```
https://docs.google.com/spreadsheets/d/[SPREADSHEET_ID]/edit
