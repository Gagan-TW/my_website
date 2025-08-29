
# Contributing to Refract Documentation

Thank you for your interest in contributing to the **Refract Documentation**!  
We welcome improvements, corrections, and additions from the community.

Whether you're fixing a typo, restructuring content, or adding new documentation, your contribution is appreciated.

## 📌 Guidelines

Please follow the steps below to contribute effectively:

### 1. **Fork the Repository**

Start by forking the repository to your GitHub account.

```bash
git clone https://github.com/<your-username>/<your-fork>.git
cd <your-fork>
````

### 2. **Create a Branch**

Always work on a new branch, never on the `main` branch.

```bash
git checkout -b update-docs-section
```

### 3. **Make Your Changes**

* Use proper Markdown syntax.
* Follow the Google Developer Style Guide.
* Keep a formal and consistent tone.
* Organize files correctly under the `/docs` folder.

### 4. **Test Locally**

Make sure your updates do not break the site:

```bash
npm install
npm run start
```

Visit `http://localhost:3000` and verify the sidebar, links, and formatting.

### 5. **Commit Your Changes**

Use meaningful commit messages:

```bash
git add .
git commit -m "Improve docs: Updated Reusing Logic section"
```

### 6. **Push and Submit a Pull Request**

Push your branch and open a pull request to the original repo.

```bash
git push origin update-docs-section
```

---

## 🧭 Directory Overview

| Folder/File            | Purpose                              |
| ---------------------- | ------------------------------------ |
| `docs/`                | All main documentation lives here.   |
| `sidebars.js`          | Controls navigation structure.       |
| `docusaurus.config.js` | Site metadata, navbar/footer config. |
| `blog/`                | Optional blog posts (if enabled).    |

---

## 💡 Contribution Ideas

* Fix typos or improve clarity
* Add diagrams or images
* Document missing features
* Suggest structure improvements
* Translate content into another language

---

## 🙌 Thank You!

Your contributions make this documentation better and more helpful for everyone.
Feel free to reach out via issues or discussions if you're unsure how to start.



