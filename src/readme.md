📋 Mini Task List App – Vue.js

📚 Description

It is a small task list application developed using Vue.js 3 with the Composition API, built with modern tooling like Vite and Node.js.

🛠 Technologies Used
✅ Vue.js 3 (Composition API)
⚡ Vite (Fast development build tool)
🟢 Node.js + npm

📁 Project Structure

mini-tasklist-vue/
├── public/
│   └── BalmerDemos.png     # Update own image
├── src/
│   ├── components/
│   │   ├── TaskForm.vue     # Add task form
│   │   └── TaskList.vue     # Task list display
│   ├── App.vue              # Main component
│   └── main.js              # App bootstrap
├── package.json
├── vite.config.js
|── index.html               # App entry point
└── README.md

🚀 Installation and Running
1. Prerequisites
Node.js (v18 or higher)
npm

2. Install Dependencies
npm install

3. Start Development Server

npm run dev
Then visit: http://localhost:5173
(Or http://localhost:3001 if configured to use a custom port.)

📄 Features
✅ Add Tasks — Add new tasks to your list.

📋 List Tasks — View all current tasks.

☑️ Mark Complete — Toggle tasks as done or not done.

❌ Delete Tasks — Remove tasks from the list.

📅 Set Due Dates — Choose a date when each task is due.

🕓 Track Creation Date — Automatically adds a creation timestamp.

🎨 Responsive UI — Clean layout with a banner and footer.

🌐 Developer Footer — Links to GitHub, LinkedIn.

🧩 Vue Components
TaskForm.vue – Handles task input, including optional due date.

TaskList.vue – Displays tasks with status and date info.

App.vue – Root component managing task state and layout.

📷 Preview
🖊️ Task input with calendar

📄 Dynamic task list with completion toggle

🔗 Footer with social and hosting info

📌 Notes
Task data is stored only in memory and will reset on page reload.

This app can be extended with local storage or backend integration.