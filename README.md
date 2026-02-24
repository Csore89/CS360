# CS360
CS-360 Portfolio Reflection: Mobile App Development
1. App Requirements and User Needs
The goal of this project was to develop a functional, user-friendly mobile application specifically a Weight Tracker app. The core requirement was to provide users with a reliable, persistent way to log their daily weight and monitor their progress over time. This addresses a fundamental user need in the health and fitness space: removing the friction from tracking data so users can focus on their actual fitness goals. The app needed to be fast, intuitive, and capable of saving data locally on the device so it could function without an internet connection.

2. User-Centered UI Design
To produce a user-centered UI, the app required distinct, focused screens: a main input screen for logging new weight entries and a history screen to view past data.

Design Strategy: I utilized Android's ConstraintLayout to ensure the UI elements were responsive and scaled correctly across different device sizes.

Success Factors: The design was successful because it adhered to mobile best practices keeping the interface uncluttered, using clear, large buttons for primary actions (like saving a weight), and using a LinearLayout combined with a RecyclerView to display the history in a clean, scrollable format. This kept the cognitive load low for the user.

3. Coding Approach and Strategies
I approached the coding process by strictly separating the visual interface from the underlying logic, a foundational principle of software engineering.

Techniques: I defined the UI entirely in XML layouts and handled the logic in Java Activity classes. I utilized the Event Listener pattern (e.g., setOnClickListener) to wait for user interactions before triggering data saves.

Future Application: This strategy of isolating the database logic (creating a dedicated DatabaseHelper class for SQLite operations) from the UI logic makes the code highly modular. In future projects, I can reuse this identical database architecture for completely different apps simply by swapping out the table columns.

4. Testing and Functional Verification
Testing was a continuous process throughout development. I utilized the Android Emulator to test the app across different simulated hardware profiles.

Importance: Testing revealed how the app handled edge cases, such as attempting to save an empty weight input or rotating the screen (which triggers the Android lifecycle to destroy and recreate the Activity).

Outcome: By testing these scenarios, I was able to implement safeguards, like disabling buttons until text was entered via a TextWatcher, ensuring the app didn't crash and the SQLite database remained uncorrupted.

5. Innovation and Overcoming Challenges
A significant challenge in mobile development is managing state and hardware resources efficiently. One area requiring innovation was navigating the Android OS permission system and lifecycle constraints. For example, ensuring that features like SMS notifications or sensor listeners were properly declared in the AndroidManifest.xml and managed within the onResume and onPause lifecycle methods. This required moving beyond basic scripting to thinking structurally about how the app interacts with the host operating system to prevent memory leaks and battery drain.

6. Highlighting Knowledge, Skills, and Experience
I was particularly successful in demonstrating my skills within the Data Persistence (SQLite) component of the app. Building the DatabaseHelper.java class from scratch to handle full CRUD (Create, Read, Update, Delete) operations demonstrated a deep understanding of mobile architecture. Successfully writing the Java logic to open a database connection, insert user input, query the history, and bind that data to the visual UI proves that I can build full-stack mobile applications that are robust, data-driven, and ready for real-world use.
