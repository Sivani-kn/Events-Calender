This project is a comprehensive College Event Calendar system. It features a secure login gateway, a dynamic dashboard with advanced filtering, and dedicated detail pages for various campus activities, ranging from academic deadlines to social festivals.

🎓 College Event Calendar sleek, responsive web application designed to help students stay organized and engaged with campus life. This project demonstrates front-end development skills, including dynamic DOM manipulation, URL parameter handling, and responsive UI/UX design.

🌟 Key Features
Secure Entry: A dedicated login page (Loginpage.html) requiring authentication to access the calendar.
Dynamic Dashboard: The Homepage.html serves as a central hub where users can:
    Filter by Category: Toggle between Club Meetings, Sports, Academic Deadlines, and Social Events.
    Filter by Date: Quickly find what’s happening on a specific day.Live Sorting: Events are automatically sorted chronologically for better planning.
Interactive Detail Pages: Every event has its own uniquely styled detail page (e.g., csh.html, basketball.html, music.html) that pulls specific data like dates and descriptions using JavaScript URL parameters.
Thematic Design: Each page features custom background imagery and color schemes that match the event's vibe (e.g., musical notes for the concert, court-side views for basketball).

🛠️ Technology Stack
HTML5: Semantic structure for all pages.
CSS3: Custom styling with a focus on glassmorphism (rgba backgrounds), flexbox, and grid layouts.
JavaScript (ES6+):Dynamic event rendering and filtering logic,URL state management via URLSearchParams,Form validation for the login portal.

📂 Project Structure
Loginpage.html-The gateway to the app with simulated authentication.
Homepage.html-The main dashboard featuring the filterable event grid.csh.html-Details for Computer Science Club meetings.
midterm.html-Academic deadline tracking for Humanities papers.
debate.html-Social/Club details for the Debate Society.
food.html-Event page for the International Food Festival.
basketball.html-Sports event page for the tournament finals.
Swim.html-Sports event page for the swimming championship.
finalexam.html-Important academic schedule release details.
music.html-Social event details for the Music Club concert.

🚀 How to RunClone this repository to your local machine.
Open Loginpage.html in any modern web browser.
Credentials-Username: user,Password: password
Explore the calendar, apply filters, and click on any event card to see its specific details!

📸 Preview-The application uses a responsive grid layout. On mobile, the filters stack vertically for easy access, and the event cards adapt to any screen size.

Future Improvements
While the current version provides a solid foundation for an event management system, the following features are planned for future releases to enhance scalability and user engagement:

1. Persistent Backend Integration
Currently, the app uses a hardcoded array of events.

Goal: Transition to a Node.js/Express backend with a MongoDB or PostgreSQL database.

Benefit: This will allow administrators to add, edit, or delete events in real-time through a secure dashboard rather than modifying the source code.

2. Advanced User Authentication
The current login system uses client-side simulation.

Goal: Implement JWT (JSON Web Tokens) or OAuth 2.0 (Login with Google/GitHub).

Benefit: This provides genuine security and allows for personalized user profiles where students can "save" or "favorite" specific events.

3. Automated Notification System
Goal: Integrate the Web Push API or an email service like SendGrid.

Benefit: Users could opt-in to receive reminders 24 hours before an event they are interested in, reducing "no-show" rates for club meetings and deadlines.

4. Interactive Campus Map
Goal: Integrate the Google Maps API or Leaflet.js.

Benefit: Each event detail page (like basketball.html or csh.html) could feature an embedded map showing exactly where on campus the event is located.

5. "Add to Calendar" Functionality
Goal: Add a button to generate .ics files or direct links to Google Calendar/Outlook.

Benefit: Seamlessly sync campus life with a student's personal digital schedule.

🧠 Technical Challenges & Solutions
The Challenge: Data Persistence Across Pages
One of the main hurdles in a purely front-end project is passing data from the Homepage.html to specific detail pages like music.html without a database.

The Solution: URL Parameter Routing
I implemented a robust "routing" logic using the JavaScript URLSearchParams interface.

Encoding: When a user clicks an event, a function captures the event's specific data (Date, Description, Title).

Transfer: The app redirects to the specific HTML template while appending this data as a query string (e.g., music.html?date=2023-11-01&desc=Concert).

Decoding: The destination page runs a script upon loading to "pluck" those values from the URL and inject them into the DOM. This allowed me to keep the detail pages lightweight and dynamic.