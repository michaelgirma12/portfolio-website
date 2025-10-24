# Michael Girma - Portfolio Website

A modern, responsive portfolio website showcasing my skills and experience as a Cloud Engineering Associate and Freelance Web Developer. This project demonstrates end-to-end cloud deployment using AWS services.

##  Features

- **Responsive Design**: Fully responsive layout that works on desktop, tablet, and mobile devices
- **Modern UI/UX**: Clean, professional design with smooth animations and transitions
- **Interactive Navigation**: Desktop navigation with mobile hamburger menu
- **Portfolio Sections**:
  - Hero section with profile picture and call-to-action buttons
  - About section with experience and education details
  - Experience section highlighting technical skills and work history
  - Projects section showcasing GitHub repositories
  - Contact section with email and LinkedIn links
- **CV Download**: Direct download link for resume
- **Social Media Integration**: Links to LinkedIn and GitHub profiles
- **View Tracking**: AWS Lambda integration for tracking website visits
- **Cloud Deployment**: Fully deployed on AWS infrastructure

## 🛠️ Technologies Used

### Frontend
- **HTML5, CSS3, JavaScript (ES6+)**
- **Styling**: Custom CSS with Google Fonts (Poppins)
- **Responsive Design**: CSS Media Queries
- **Version Control**: Git

### AWS Cloud Infrastructure
- **AWS S3**: Static website hosting and file storage
- **AWS CloudFront**: Content Delivery Network (CDN) for global distribution
- **AWS Route 53**: DNS management and domain routing
- **AWS Lambda**: Serverless functions for view tracking API
- **AWS DynamoDB**: NoSQL database for storing view analytics
- **AWS API Gateway**: RESTful API endpoints for backend services

##  AWS Architecture

This project demonstrates a complete cloud deployment pipeline using AWS services:
nternet → Route 53 → CloudFront → S3 (Static Website)
↓
API Gateway → Lambda → DynamoDB (View Tracking)


### Deployment Architecture Details:
- **S3 Bucket**: Hosts the static website files (HTML, CSS, JS, images)
- **CloudFront Distribution**: Provides global CDN with caching for improved performance
- **Route 53**: Manages DNS routing and custom domain configuration
- **Lambda Function**: Processes view tracking requests and updates analytics
- **DynamoDB Table**: Stores view count and analytics data
- **API Gateway**: Exposes RESTful endpoints for the Lambda functions

portfolio-website/
├── assets/
│ ├── about me pic .png # About section image
│ ├── arrow.png # Navigation arrow icon
│ ├── checkmark.png # Experience checkmark icons
│ ├── Cloud associate eng.pdf # Resume/CV file
│ ├── education.png # Education section icon
│ ├── email.png # Email contact icon
│ ├── experience.png # Experience section icon
│ ├── github.png # GitHub social media icon
│ ├── ISO_C++Logo.svg.png # C++ project logo
│ ├── java_logo_1067x1201.png # Java project logo
│ ├── linkedin.png # LinkedIn social media icon
│ ├── new_cpp_ logo.png # C++ project logo
│ └── portfoilo headshot f.png # Main profile picture
├── index.html # Main HTML file
├── style.css # Main stylesheet
├── mediaqueries.css # Responsive design styles
└── script.js # JavaScript functionality


## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- AWS CLI (for deployment)
- AWS Account with appropriate permissions

### Local Development

1. **Clone the repository**:
   ```bash
   git clone https://github.com/michaelgirma12/portfolio-website.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd portfolio-website
   ```

3. **Open in browser**:
   - Option 1: Open `index.html` directly in your browser
   - Option 2: Use a local server (recommended for development):
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js
     npx serve .
     
     # Using PHP
     php -S localhost:8000
     ```

4. **Access the website**:
   - Direct file: `file:///path/to/index.html`
   - Local server: `http://localhost:8000`

### AWS Deployment

1. **Configure AWS CLI**:
   ```bash
   aws configure
   ```

2. **Deploy to S3**:
   ```bash
   aws s3 sync . s3://your-bucket-name --delete
   ```

3. **Configure CloudFront**:
   - Create CloudFront distribution pointing to S3 bucket
   - Configure caching behaviors and error pages

4. **Set up Route 53**:
   - Create hosted zone for your domain
   - Configure DNS records to point to CloudFront

5. **Deploy Lambda Function**:
   ```bash
   # Package and deploy Lambda function for view tracking
   aws lambda create-function --function-name portfolio-view-tracker
   ```

6. **Configure API Gateway**:
   - Create REST API
   - Set up Lambda integration
   - Deploy API to production stage

## 📱 Responsive Design

The website is fully responsive with breakpoints at:
- **Desktop**: 1400px and above
- **Tablet**: 1200px - 1399px
- **Mobile**: 600px - 1199px
- **Small Mobile**: Below 600px

## 🎨 Customization

### Updating Personal Information

1. **Profile Information**: Edit the hero section in `index.html` (lines 44-46)
2. **About Section**: Update the about text in `index.html` (lines 99-104)
3. **Experience**: Modify skills and experience in `index.html` (lines 120-252)
4. **Projects**: Update project links and descriptions in `index.html` (lines 261-312)
5. **Contact**: Change contact information in `index.html` (lines 314-335)

### Styling Changes

- **Colors**: Modify color variables in `style.css`
- **Fonts**: Change the Google Fonts import in `style.css` (line 4)
- **Layout**: Adjust spacing and sizing in `style.css`
- **Responsive Design**: Update breakpoints in `mediaqueries.css`

### Adding New Sections

1. Add HTML structure in `index.html`
2. Add corresponding CSS styles in `style.css`
3. Update navigation links
4. Add responsive styles in `mediaqueries.css`

## 🔧 Technical Details

### JavaScript Functionality

- **Mobile Menu Toggle**: Hamburger menu animation and functionality
- **Smooth Scrolling**: CSS-based smooth scrolling between sections
- **View Tracking**: AWS Lambda API integration for analytics via API Gateway

### CSS Features

- **Flexbox Layout**: Modern CSS layout system
- **CSS Transitions**: Smooth hover effects and animations
- **Custom Properties**: Consistent styling approach
- **Mobile-First Design**: Responsive design principles

### AWS Services Integration

- **S3 Static Hosting**: Efficient file storage and serving
- **CloudFront CDN**: Global content delivery with edge caching
- **Lambda Serverless**: Scalable backend processing
- **DynamoDB**: Fast, scalable NoSQL database
- **API Gateway**: RESTful API management and throttling
- **Route 53**: Reliable DNS management

### Performance Optimizations

- Optimized images in the assets folder
- Minimal JavaScript for fast loading
- Efficient CSS with minimal redundancy
- External font loading optimization
- CloudFront caching for improved global performance
- S3 static website hosting for cost-effective delivery

## Live Demo

Visit the live website: https://cloudportfolio.michael-girma.com/ 

##  Contact

- **Email**: mikework1224@gmail.com
- **LinkedIn**: [Michael Girma](https://www.linkedin.com/in/michaelgirma12)
- **GitHub**: [michaelgirma12](https://github.com/michaelgirma12)

## License

This project is open source and available under the [MIT License](LICENSE).

##  Contributing

Contributions, issues, and feature requests are welcome! 

##  Acknowledgments

- Design inspiration from modern portfolio websites
- Google Fonts for typography
- AWS for cloud infrastructure and services
- Open source community for tools and resources

---




## 📁 Project Structure
