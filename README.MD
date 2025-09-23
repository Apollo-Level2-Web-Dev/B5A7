# B5A7 - Portfolio

---

## 🌐 My Portfolio Website – Requirements (NextJS + Prisma + ExpressJS)

### **Project Overview**

Design and build a **personal portfolio website** with the following core features, ensuring good **SEO** practices are implemented for better discoverability:

- **Authentication & Authorization**: Implement a system where users can log in to access private features.
- **Blog Management**: Create a dynamic blog management system that allows you to create, read, update, and delete blogs.
- **About Me Section**: Display personal information, work background, and skills.
- **Projects Showcase**: Include a section for personal projects.
- **Resume Builder**: Implement an interactive **SSR** form that allows users to create and download their resume as a **PDF**.
- **Dashboard**: A centralized dashboard to manage blog posts, resume building, and view dynamic project content.
- Responsive UI and polished UX.

---

### **Tech Stack**

- **Frontend Framework**: NextJS
- **Language**: TypeScript
- **Styling**: Tailwind CSS (with responsive utility classes) or other css frameworks
- **Backend**: Node.js/Express, Prisma with Postgres, JWT + bcrypt (Secure Authentication)
- **Optional Enhancements**: react-hot-toast (notifications)

---

### **📌 Minimum Requirements**

- **✅ Authorization & Authentication:**
  - Use **JWT-based authentication**.
  - Users must register and log in to access private features.
  - Passwords securely hashed (bcrypt or equivalent)
- **✅ Blog Management:**
  - Users should be able to view all blogs and individual blog posts.
  - Use **ISR** for the "All Blogs" page to fetch new content without rebuilding the entire site.
  - Use ISR with getStaticPaths + revalidate for individual blog pages to generate content dynamically for each user request.
  - **Dynamic SEO:** Ensure that the **meta title** and **description** tags are dynamically generated for each blog post. Include **Open Graph** and **Twitter Card** tags to optimize content for sharing on social media.
- ✅ **About Me Section**:
  - This section should include static personal details (name, contact info, bio, etc.).
  - Fetch static content using **SSG** for fast performance.
  - Implement **SEO tags**: Dynamic meta title and description based on the About Me content.
- ✅ **Project Showcase**:
  - A section dedicated to personal projects with **thumbnail**, **project link**, **live site**, **description, and features**.
  - Use **SSR** or **ISR** to allow dynamic updates or fetching of project data.
  - **SEO considerations**: Use dynamic meta tags for project pages to enhance visibility and social media sharing.
- ✅ **Resume Builder**:
  - Implement the Resume Builder as an SSR-rendered page with a client-side PDF generation feature, allowing users to input data and download a customized resume
  - The resume should include sections like **Contact Information**, **Work Experience**, **Education**, **Skills**, etc.
  - **SEO**: Ensure that the **Resume Builder page** has dynamic title and description tags for search engine optimization.
  - Resume Builder be visible even if user is not logged in, but only accessible to authenticated users.
- ✅ **Dashboard**:
  - A dynamic **admin only dashboard** where users can manage blog posts, view statistics, and generate reports.
- ✅ **Private Pages**:
  - Protect the **resume builder** and other private features using **JWT**.
  - Only authenticated users should be able to access these features.
- ✅ **Rich Text Editor**:
  - Use a **rich text editor** to create, edit, and format blog/project content.
  - Include options like bold, italic, links, images, etc.

### **🧠 Design Thinking Guide**

Think through the following aspects to ensure clean and scalable logic:

- **Authentication**: How will you handle **JWT expiration** and **refresh tokens**? Will you implement **third-party login** services (e.g., Google)?
- **Dynamic Content**: Blog content, projects, and resume data should be easily **updateable** without requiring site rebuilds.
- **Dashboard**: What dynamic statistics or features will the dashboard provide for the admin (blog post views, resume created, etc.)?
- **SEO for Blogs**: How will you handle **SEO optimization** for blog posts? Consider implementing **dynamic meta tags** for each blog post based on the content.

---

### **📜 Access & Visibility**

- **Blog Access**: Can authenticated users **edit** their blogs, or only admins? Should all blogs be visible to the public, or only some?
- **Private Pages**: The **resume builder** and **admin dashboard** should only be accessible to authenticated users?
- **Admin Dashboard**: Should it include **analytics** such as number of views on blog posts or the number of resumes generated?

---

### **🔐 Role-Based Access Control**

- Implement **JWT-based role-based route protection** for private areas like the resume builder and dashboard.
- The **Blog Management** system should allow for role-based access:
  - **Admin**: Can create, edit, and delete any blog post.
- **Resume Builder** should be accessible only to **authenticated users**.

---

### **❄️ General UI/UX Enhancements**

- Interactive elements: carousels, dynamic stat cards, responsive charts etc.
- Skeleton and smooth transitions for enhanced perceived performance and global error handling.
- No broken links or non-functional buttons.
- Accessibility-compliant components and semantic HTML.
- Lazy-loading for heavy assets.
- Data visualization components like cards, bar charts, pie charts, and tables—all dynamically updated.
- **Strict Error Handling (⚠️ Mandatory for Full Marks)**:
  - All **forms must implement proper validation and error messages** (e.g., required fields, invalid email, password mismatch).
  - Clear and user-friendly error messages for network/API failures, validation errors, and unauthorized actions.
  - Toast/alert message for both success and error states (e.g., `react-hot-toast`).
  - ⚠️ **Important:** If you fail to handle form validation errors or API errors properly, **your marks will be significantly reduced.**

---

### **Submission Guidelines**

1. **Codebase**
   - Clean, modular codebase following best practices.
   - Comprehensive README.md including:
     - Live deployment link
     - Project overview
     - Project features
     - Technology stack
     - Setup instructions
     - Any other relevant notes
2. **GitHub Repository**
   - Separate/Mono repositories for Frontend and Backend.
   - Commit history showing development progress (minimum 10 meaningful commit messages for each frontend and backend repo; otherwise, you will get 0).
3. **Live Deployment**
   - Provide live deployment URLs for both frontend and backend.
4. **Demo video** (5-10 minutes) walkthrough
5. **Credentials**
   - Provide admin login details (email & password) for testing

### **📅 Deadline & Marking Scheme**

| **Submission Date**                          | **Marks Available** |
| -------------------------------------------- | ------------------- |
| On or before **October 03, 2025 – 11:59 PM** | 🟢 Full 60 Marks    |
| After **October 03, 2025**                   | 🔴 30 Marks Max     |

---

### **🚫 Academic Integrity**

Plagiarism of any kind will result in **0 marks**.

Make sure your submission reflects **your own original work**.

You may use online references, but you must write your own code.

---

📌 _This assignment is designed to test your ability to design, implement, and secure a portfolio system using NextJs + Prisma + ExpressJs. It reflects real-world API architecture challenges, so focus on correctness, clarity, and robustness._
