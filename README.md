# Sangam Verse - Social Media Website
Sangam Verse is a social media platform that connects users through profiles, secure login, and versatile content sharing, including posts, images, and multimedia. Users can create groups, follow others, and pin key posts. With email verification, Sangam Verse ensures authenticity, providing a dynamic, secure space for communication and community-building.

## Features
- **User Authentication:** Secure user registration and login system.
- **Profile Management:** Users can create and edit their profiles.
- **Post Creation & Sharing:** Users can create, edit, and share posts.
- **Real-Time Comments:** Users can comment on posts in real-time.
- **Follow System:** Follow other users to stay updated with their activities.
- **Interactive Notifications:** Get notified of new followers, comments, and likes.
- **Responsive Design:** A fluid and responsive UI that adapts to desktop and mobile devices.

## Technology Used
- **Backend:** Laravel framework, a PHP-based backend framework that offers a well-organized and secure environment for server-side processing.
- **Frontend:** Vue.js combined with Inertia.js to create dynamic single-page applications (SPA) with server-side rendering.
- **Containerization:** Docker and Laravel Sail for easy setup, development, and deployment within a consistent environment.
- **Database:** MySQL for storing user data, posts, comments, and follow relationships efficiently.

## Architecture
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939459/Sangam_Verse/sangam-verse_architecture_hukilj.png"/>


## Entities and Relationships Diagram(ERD)
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939460/Sangam_Verse/sangam-verse_ER_diagram_svacvd.png"/>

## Website Snapshot
#### Create an Account:
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939458/Sangam_Verse/create_account_jq0aoa.png"/>

#### Login:
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939458/Sangam_Verse/login_pbdwcl.png"/>

#### Main Dashboard:
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939459/Sangam_Verse/dashboard_r4iroc.png"/>

#### User Profile Dashboard:
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939458/Sangam_Verse/user-profile_dashboard_dwlz8l.png"/>

#### Group Dashboard:
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1729939459/Sangam_Verse/group_dashboard_wb9inf.png"/>

#### Local Mailpit Server:
<img width="950px;" src="https://res.cloudinary.com/cloud-alpha/image/upload/v1730144053/Sangam_Verse/sangam-verse_Mailpt_zaspe3.png"/>

## Prerequisites
- *Docker & Docker Compose*
- *Node.js & npm*
- *Composer*

## Installation with Docker

1. Clone the project `git clone https://github.com/yourusername/sangam-verse.git`
2. Run `composer install` - Navigate into the project folder and run:
```bash 
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php83-composer:latest \
    composer install --ignore-platform-reqs
```
3. Copy `.env.example` to `.env`: Run command into the terminal `cp .env.example .env`
4. Start the project in detached mode: `./vendor/bin/sail up -d`
5. To run any `artisan` command, first access the Docker container: `./vendor/bin/sail bash`
6. Set encryption key: `php artisan key:generate --ansi`
7. Run migrations: `php artisan migrate`