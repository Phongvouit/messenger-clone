Real-Time Messenger Clone

## Project Description

This project is a state-of-the-art real-time messenger clone, developed using powerful and cutting-edge technologies to create a fully functional and visually stunning chat application. It aims to provide an immersive and interactive user experience by leveraging real-time communication capabilities

## Key Features

The messenger clone includes a wide range of features:

• Real-time Messaging and Notifications: Achieved through the integration of Pusher, ensuring an interactive user experience.

• Secure User Authentication: Implemented using NextAuth.js to manage user authentication and protect sensitive data.

• Social Login: Supports convenient sign-up and login via popular platforms like Google and GitHub.

• Efficient Form Handling: Utilizes React Hook Form for seamless management of user input.

• Image Uploads: Leverages Cloudinary for managing and uploading images within the application.

• Robust Database Solution: Combines Prisma with MongoDB for an efficient and scalable backend capable of handling many users and conversations.

• Conversation Management: Users can create personal and group chats. Conversations are ordered by the last message sent, and the view automatically scrolls to the newest message. It also shows real-time "seen" status for messages.

• User Status Display: Shows online/offline status of users in real-time using Pusher's presence channels.

• User Settings: Allows users to update their name and avatar.
• Conversation Deletion: Provides functionality to delete conversations with a confirmation step.

• Image Modals: Sent images can be opened in a larger modal view upon clicking.

• Optimized User Experience: Incorporates loading states to improve application responsiveness, reducing "dead moments".

## Technologies Used

The project is built with a modern technology stack, including:
• Frontend Framework: Next.js, React.js

• Styling: Tailwind CSS, Headless UI

• Database: Prisma, MongoDB

• Authentication: NextAuth.js (supporting Google and GitHub OAuth, and email/password credentials)

• Real-time Communication: Pusher (for real-time messages, notifications, and presence tracking)

• Image Upload: Cloudinary

• Form Handling: React Hook Form

## How to Set Up and Run the Project

1. Clone the project
```bash
https://github.com/Phongvouit/messenger-clone.git
```

2. Install Dependencies
```bash
npm install
```
3. Configure Environment Variables

4. Configure next.config.js

5. Update tailwind.config.js

6. Push Prisma Schema to Database
```bash
npx prisma db push
```

7. Run the Application
```bash
npm run dev
```


