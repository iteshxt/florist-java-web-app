# Florist Landing Page

A beautiful, modern Spring Boot landing page for a florist business with integrated Maven-Docker pipeline.

## Features

- **Single Page Landing** - Clean, flat minimal design (no rounded corners)
- **Hero Section** - Stunning full-screen hero with CTA
- **Why Choose Us** - Benefits showcase with numbered cards
- **Gallery** - Beautiful flower collection showcase
- **Booking CTA** - Strong call-to-action for bookings
- **Contact Section** - Business information and hours
- **Responsive Design** - Perfect on all devices
- **Maven-Docker Integration** - Automated Docker build on deploy

## Project Structure

```
florist-app/
├── src/main/java/com/florist/
│   ├── FloristApplication.java
│   └── controller/HomeController.java
├── src/main/resources/
│   ├── templates/index.html    # Single landing page
│   ├── static/style.css        # Flat minimal styling
│   └── application.properties
├── Dockerfile                  # Alpine-based container
├── pom.xml                     # Maven config
└── README.md
```

## Requirements

- Java 17+
- Maven 3.6+
- Docker (optional, for containerization)

## Build & Run

### Local Development

```bash
# Build the application
mvn clean package

# Run locally
mvn spring-boot:run
```

Access at: `http://localhost:8080`

### Docker Build

```bash
# Build with Docker image
mvn clean package

# Note: Docker build only happens on 'mvn deploy' phase
# To build image without deploy:
mvn docker:build
```

## Maven-Docker Integration

Uses **dockerfile-maven-plugin** for seamless containerization:

### Build Process
- `mvn clean package` → builds JAR + runs tests
- `mvn deploy` → builds Docker image and pushes to registry

### Configuration

Edit `pom.xml` to customize:
- `<docker.image.prefix>` - Docker Hub username
- `<tag>` - Image version (matches Maven version)

### Push to Docker Hub

```bash
# Set Docker credentials first
mvn deploy
```

## Design Philosophy

✨ **Flat Minimal** - No rounded corners, clean lines  
✨ **Typography-First** - Professional sans-serif fonts  
✨ **Generous Spacing** - Breathing room between elements  
✨ **Color Palette** - Dark backgrounds, red accents  
✨ **Smooth Interactions** - 0.3s transitions on hover  
✨ **Mobile Optimized** - Fully responsive layout  

## Page Sections

| Section | Purpose |
|---------|---------|
| **Navbar** | Navigation and branding |
| **Hero** | Full-screen hero with main CTA |
| **Why Choose Us** | 4 reason cards with benefits |
| **Gallery** | 6 flower collection showcase |
| **Booking CTA** | Prominent booking section |
| **Contact** | Address, phone, hours |
| **Footer** | Copyright and tagline |

## Technologies

- **Backend**: Spring Boot 3.1.5
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Container**: Docker with Alpine JRE
- **Build**: Maven 3.6+
- **Language**: Java 17+

## Smooth Scrolling

All navigation links support smooth scroll:
- Click any nav link to smoothly scroll to section
- "Book Now" CTA scrolls to booking section

## Customization

### Change Colors
Edit CSS variables in `style.css`:
```css
:root {
    --primary: #1a1a1a;      /* Main color */
    --accent: #d63031;       /* CTA button color */
    --light: #f5f5f5;        /* Background */
}
```

### Update Content
Edit `index.html` to change:
- Business name and tagline
- Service offerings
- Contact information
- Social media links (add in footer)

## DevOps Pipeline

**Benefits:**
✅ Single command build  
✅ Version alignment (Maven version = Docker tag)  
✅ Automated registry push  
✅ CI/CD ready (GitHub Actions, GitLab CI, Jenkins)  
✅ No manual Docker commands needed  

## License

MIT License - Build beautiful businesses!

