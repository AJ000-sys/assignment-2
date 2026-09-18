# assignment-2

# Project Description
This site was built for the Office of Student Engagement to help students discover and get involved in campus life such as clubs, service opportunities, cultural events, and social activities. It is built around two pages:

- index.html - the homepage, with a hero section, a grid of upcoming events, and an "About Us" section describing the office's mission.

- event.html - a single event detail template, used for the Annual Involvement Fair, with a full description, schedule, sidebar info card, and related events.

The intended audience is current and prospective students looking for ways to get involved on campus.

# Layout Decisions
Flexbox is used whenever content needs to align, space itself out, or wrap along a row or column.

- nav ul (main navigation) and .footer-nav ul (footer navigation) center the links, add consistent gap spacing, and let them wrap onto a new line on narrow screens.

- .hero-container stacks the hero heading, image, paragraph, and button in a centered column with even spacing.

- .related-events-list lays out the related-event cards in a row that wraps (flex-wrap: wrap) when there isn't room for all of them side by side.

- .event-card, .related-event-card, and .event-sidebar each use a flex column internally so an image, heading, text, and button stack in order, with justify-content: space-between keeping the button pinned to the bottom of the card even when descriptions vary in length.

Flexbox fit these cases because they're all a single row or column of items that need to align and space themselves relative to each other.

CSS Grid is used in the two places that need a genuine two-dimensional layout:

- .events-grid (index.html) arranges the upcoming event cards into rows and columns at once, so cards line up both horizontally and vertically.

- .event-details (event.html) creates the two-column layout for the event's main content and its info sidebar, using grid-template-columns: 2fr 1fr so the main content column is wider than the sidebar.

Grid fit these cases because both layouts have independent rows and columns that need to be controlled together.

# Responsive Design
The site uses two breakpoints, both defined with max-width media queries:

- @media (max-width: 700px) (event.html): .event-details collapses from a two-column grid (2fr 1fr) to a single column (1fr). The sidebar and main content are reordered so .event-main appears first (order: 1) and .event-sidebar appears second (order: 2) on small screen.

- @media (max-width: 500px) (global): nav ul switches from a horizontal row (flex-direction: row) to a vertical column (flex-direction: column) and reduces the gap from 20px to 10px, so the main navigation links stack neatly on very narrow screens.

# Semantic HTML
- (header) — wraps the site logo/title and main navigation on every page.

- (nav) — used for both the main site navigation and the footer navigation, identifying these link groups as navigation for assistive technology and search engines.

- (main) — wraps the primary, unique content of each page, distinguishing it from repeated header/footer content.

- (footer) — wraps the copyright notice, contact link, and footer navigation, marking it as the closing/site-info section of the page.

# Sources
(hero.jpeg), 
Jensen, Marcus. "USU Recognized for Its Commitment to Trees on Campus." USU Today, Utah State University, 23 Sept. 2021, www.usu.edu/today/story/usu-recognized-for-its-commitment-to-trees-on-campus.

(event1.jpg), 
Orozco B., Darlene. "Students Explore New Interests at Annual Involvement Fair." Eastern Connecticut State University, 10 Sept. 2025, www.easternct.edu/news/_stories-and-releases/2025/september/students-explore-new-interests-at-annual-involvement-fair.html.

(event2.jpeg), 
Mesa PTO. "[Multicultural Festival logo with international flags]." Multicultural Event at Mesa, 3 Feb. 2026, www.mesapto.com/multicultural-festival.html

(event3.png), 
"Late Night Breakfast." Get Involved, Wayne State University, 27 Apr. 2022, getinvolved.wayne.edu/event/7159385

(event4.jpg), 
"Leadership Framework." Leadership, University of Alberta, www.ualberta.ca/en/human-resources-health-safety-environment/learning-and-development/leadership-development/index.html

(event5.png), 
"Community Service Concept Hands Various Colors." Shutterstock, www.shutterstock.com/image-vector/community-service-concept-hands-various-colors-1115565305