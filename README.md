# Cloud Resume Challenge - Portfolio Website

## 🚀 Overview

A modern, responsive portfolio website built as part of the Cloud Resume Challenge. This project showcases my skills as a Cloud/DevOps Engineer through a dark-themed, professional portfolio with interactive elements and modern design.

🌐 **Live Site**: [rafftec.click](https://rafftec.click)

## ✨ Features

- **Dark Mode Design** with bright accent colors
- **Responsive Layout** that works on all devices
- **Modern UI/UX** with smooth animations and hover effects
- **Professional Sections**:
  - Hero/Landing page
  - About Me
  - Experience & Skills
  - Certifications & Badges
  - Projects showcase
  - Blog section
  - Contact information

## 🛠️ Technologies Used

- **Frontend**: HTML5, CSS3, JavaScript
- **Styling**: Custom CSS with CSS Grid and Flexbox
- **Fonts**: Inter (Google Fonts)
- **Icons**: Custom icon assets
- **Responsive Design**: Mobile-first approach

## 📁 Project Structure

```
Cloud-Resume-Challenge-/
├── website/
│   ├── index.html          # Main HTML file
│   ├── style.css           # Main stylesheet
│   ├── mediaqueries.css    # Responsive design styles
│   ├── script.js           # JavaScript functionality
│   └── assets/             # Images and icons
│       ├── profile-pic.jpg
│       ├── about-pic.jpg
│       ├── project-*.png
│       └── *.png (icons)
└── README.md
```

## 🎨 Design Features

### Color Scheme
- **Primary**: Bright cyan (#00d4ff)
- **Secondary**: Coral red (#ff6b6b)
- **Accent**: Teal (#4ecdc4)
- **Background**: Deep black (#0a0a0a)
- **Cards**: Dark gray (#111111)

### Key Components
- Fixed navigation with backdrop blur
- Grid-based hero section
- Card-based project and certification displays
- Responsive hamburger menu for mobile
- Smooth scroll behavior
- Hover animations with glow effects

## 📱 Responsive Design

The website is fully responsive with breakpoints at:
- **Desktop**: 1200px+
- **Tablet**: 768px - 1199px
- **Mobile**: 480px - 767px
- **Small Mobile**: <480px

## 🏗️ Architecture

![Architecture Diagram](./Architecture%20diagram.png)

The portfolio website follows a modern serverless architecture pattern with:
- **Frontend**: Static HTML/CSS/JS hosted on AWS S3
- **CDN**: CloudFront for global content delivery
- **DNS**: Route 53 for custom domain management
- **SSL**: AWS Certificate Manager for HTTPS
- **CI/CD**: GitHub Actions for automated deployment

## 🛠️ Troubleshooting

### Route 53 Multiple Hosted Zones Error
If you encounter "multiple Route 53 Hosted Zones matched" error:

```hcl
# In modules/route53_acm/main.tf, add zone_id constraint:
data "aws_route53_zone" "dns_zone" {
  name         = var.domain_name
  private_zone = false
  # Add this line with your specific zone ID:
  zone_id      = "Z1234567890ABC"  # Replace with actual zone ID
}
```

Or use tags to identify the correct zone:
```hcl
data "aws_route53_zone" "dns_zone" {
  name         = var.domain_name
  private_zone = false
  tags = {
    Environment = "production"
  }
}
```

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/Amraff/Cloud-Resume-Challenge-.git
   ```

2. **Navigate to the website directory**
   ```bash
   cd Cloud-Resume-Challenge-/website
   ```

3. **Open in browser**
   - Open `index.html` in your web browser
   - Or use a local server for development

## 📂 Sections Overview

### 🏠 Hero Section
- Professional introduction
- Call-to-action buttons
- Social media links
- Profile image with glow effect

### 👨‍💻 About Me
- Professional summary
- Experience highlights
- Education information
- Skills overview

### 💼 Experience
- Technical skills categorized by expertise level
- DevOps and Cloud technologies
- Tools and frameworks

### 🏆 Certifications
- AWS certifications
- DevOps & Cloud certifications
- Digital badges
- Organized by category with expiration dates

### 🚀 Projects
- **Digi-Voice**: AI-powered voice processing system
- **Reddit Clone Deployment**: DevOps deployment with CI/CD
- **Cloud Resume Challenge**: Serverless AWS website
- Additional portfolio projects
- Each with GitHub links and architecture diagrams

### 📝 Blog
- Technical articles
- DevOps best practices
- Cloud architecture insights

### 📞 Contact
- Email and LinkedIn links
- Professional contact information

## 🔧 Customization

To customize this portfolio for your own use:

1. **Update personal information** in `index.html`
2. **Replace images** in the `assets/` folder
3. **Modify colors** in the CSS custom properties
4. **Update project links** and descriptions
5. **Add your own certifications** and experience

## 📈 Performance Features

- Optimized images
- Minimal JavaScript
- CSS custom properties for consistent theming
- Smooth animations with CSS transitions
- Mobile-first responsive design

## 🌐 Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Mobile browsers

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to fork this project and customize it for your own portfolio. If you have suggestions for improvements, please open an issue or submit a pull request.

## 📧 Contact

- **LinkedIn**: [Raphew Karim Issah](https://www.linkedin.com/in/raphew-karim/)
- **GitHub**: [@Amraff](https://github.com/Amraff)
- **Email**: raphewkarim@gmail.com

---

⭐ **Star this repository if you found it helpful!**