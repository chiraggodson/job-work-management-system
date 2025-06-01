# Job Work Management System

A modern, responsive web application for managing job work orders in textile/fabric production. Built with Next.js, TypeScript, and Tailwind CSS with a sleek black and white design with red accents.

## 🚀 Features

- **Create Job Orders**: Add new job orders with fabric name, party name, yarn used, and total quantity
- **Track Production**: Update production quantities with decimal precision (up to 2 decimal places)
- **Real-time Progress**: Visual progress bars and status tracking
- **Modern UI**: Clean black and white design with red accent colors
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Status Management**: Automatic status updates (Pending, Completed, Canceled)

## 🛠️ Technology Stack

- **Frontend**: Next.js 15.3.2 with TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: Shadcn/ui
- **Icons**: Lucide React
- **Build Tool**: Turbopack
- **Data Storage**: Google Sheets API
- **Backend**: Next.js API Routes

## 📋 Prerequisites

Before running this application, make sure you have:

- Node.js 18.0 or higher
- npm or yarn package manager

## 🔧 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd job-work-management
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🚀 Deployment Options

### Option 1: Vercel (Recommended)
1. Push your code to GitHub
2. Visit [vercel.com](https://vercel.com)
3. Import your GitHub repository
4. Deploy with one click

### Option 2: Netlify
1. Push your code to GitHub
2. Visit [netlify.com](https://netlify.com)
3. Connect your GitHub repository
4. Deploy automatically

### Option 3: Railway
1. Visit [railway.app](https://railway.app)
2. Connect your GitHub repository
3. Deploy with automatic builds

## 📱 Usage Guide

### Creating a Job Order
1. Fill in the form with:
   - **Fabric Name**: Name of the fabric being produced
   - **Party Name**: Customer/client name
   - **Yarn Used**: Type of yarn being used
   - **Total Order Quantity**: Total quantity to produce (supports decimals)

2. Click "Create Job Order" to add it to the system

### Updating Production
1. Find your job order in the table
2. Click the "Update" button
3. Enter the additional quantity produced (supports up to 2 decimal places)
4. Click "Update Production" to save

### Monitoring Progress
- View real-time progress bars for each order
- Check status indicators (Pending, Completed, Canceled)
- Monitor remaining quantities

## 🎨 Design Features

- **Black & White Theme**: Professional and clean appearance
- **Red Accents**: Strategic use of red for highlights and CTAs
- **Responsive Layout**: Adapts to all screen sizes
- **Modern Typography**: Clean, readable fonts
- **Smooth Animations**: Subtle transitions and hover effects

## 📊 Data Management

### Google Sheets Integration

The application uses Google Sheets as a database for:
- Storing job orders
- Tracking production updates
- Maintaining order status
- Real-time data synchronization

**Benefits:**
- No complex database setup required
- Easy to view and edit data directly in Google Sheets
- Familiar interface for data management
- Built-in backup and version history
- Collaborative access for team members

### Credentials Setup

1. Follow the detailed instructions in [CREDENTIALS_SETUP.md](CREDENTIALS_SETUP.md) to:
   - Create a Google Cloud project
   - Set up a service account
   - Generate credentials
   - Configure your Google Sheet

2. Set up your credentials:
   ```bash
   # Copy the credentials template
   cp src/lib/credentials.template.json src/lib/credentials.json
   
   # Update with your service account details
   nano src/lib/credentials.json
   ```

3. Important security notes:
   - Never commit credentials.json to version control
   - Keep your service account email and private key secure
   - Regularly rotate service account keys
   - Monitor API usage in Google Cloud Console

## 🔒 Security Considerations

For production deployment:
- Implement user authentication
- Add data validation
- Set up HTTPS
- Configure environment variables
- Add rate limiting

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support and questions:
- Create an issue in the GitHub repository
- Contact the development team

## 🔄 Version History

- **v1.0.0** - Initial release with basic job order management
- **v1.1.0** - Added decimal precision support for production quantities
- **v1.2.0** - Enhanced UI with black/white/red theme

---

**Built with ❤️ for efficient production management**
