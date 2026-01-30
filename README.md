# Big Data Management - Semantic Web & Knowledge Graphs

A comprehensive learning website for Big Data Management course focusing on Semantic Web and Knowledge Graphs.

## 📚 Course Content

### Week 1: Foundations
- **Lecture 11**: Introduction to Big Data Management
- **Lecture 12**: Knowledge Graphs
- **Lecture 13**: Semantic Web Technologies

### Week 2: Knowledge Representation
- **Lecture 21**: RDF & RDFS
- **Lecture 22**: Introduction to OWL

## 🗂️ Directory Structure

```
semantic-web-course/
│
├── index.html                          # Main landing page
│
├── lectures/                           # Lecture slides (PDF)
│   ├── W1_L11_introduction.pdf
│   ├── W1_L12_knowledge_graph.pdf
│   ├── W1_L13_sw_technologies.pdf
│   ├── W2_L21_knowledge_representation.pdf
│   └── W2_L22-intro_OWL.pdf
│
├── explanations/                       # Interactive explanations
│   ├── rdf_explanation.html
│   ├── rdfs_explanation.html
│   ├── owl_explanation.html
│   └── skos_explanation.html
│
├── examples/                           # Interactive examples
│   └── knowledge_graph_example.html
│
├── quizzes/                           # Practice quizzes
│   ├── semantic_web_mastery_quiz.html
│   ├── ultimate_quiz.html
│   └── interactive_exam_practice.html
│
└── revision/                          # Study materials
    └── revision_notes.html
```

## 🚀 Deployment to GitHub Pages

### Step 1: Organize Your Files

1. Create a new folder called `semantic-web-course`
2. Copy `index.html` to the root of this folder
3. Create the following subdirectories:
   - `lectures/`
   - `explanations/`
   - `examples/`
   - `quizzes/`
   - `revision/`

4. Move files to their respective directories:

**lectures/**
- W1_L11_introduction.pdf
- W1_L12_knowledge_graph.pdf
- W1_L13_sw_technologies.pdf
- W2_L21_knowledge_representation.pdf
- W2_L22-intro_OWL.pdf

**explanations/**
- rdf_explanation.html
- rdfs_explanation.html
- owl_explanation.html
- skos_explanation.html

**examples/**
- knowledge_graph_example.html

**quizzes/**
- semantic_web_mastery_quiz.html
- ultimate_quiz.html
- interactive_exam_practice.html

**revision/**
- revision_notes.md (rename to revision_notes.html if needed)

### Step 2: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the "+" icon in the top right and select "New repository"
3. Name your repository (e.g., `semantic-web-course`)
4. Make it public
5. Click "Create repository"

### Step 3: Upload Files

**Option A: Using GitHub Web Interface**
1. On your new repository page, click "uploading an existing file"
2. Drag and drop all folders and files
3. Commit the changes

**Option B: Using Git Command Line**
```bash
cd semantic-web-course
git init
git add .
git commit -m "Initial commit: Big Data Management course website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/semantic-web-course.git
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository settings
2. Scroll down to "Pages" section (left sidebar)
3. Under "Source", select "main" branch
4. Select "/ (root)" folder
5. Click "Save"
6. Wait 1-2 minutes for deployment
7. Your site will be available at: `https://YOUR-USERNAME.github.io/semantic-web-course/`

## 🎨 Features

- ✅ Responsive design that works on mobile and desktop
- ✅ Clean, modern interface with gradient background
- ✅ Organized by week and lecture
- ✅ Interactive examples and quizzes
- ✅ Easy navigation
- ✅ GitHub Pages ready (no server-side code)

## 📱 Access Your Website

Once deployed, you can access:
- **Homepage**: `https://YOUR-USERNAME.github.io/semantic-web-course/`
- **Lectures**: `https://YOUR-USERNAME.github.io/semantic-web-course/lectures/W1_L11_introduction.pdf`
- **Quizzes**: `https://YOUR-USERNAME.github.io/semantic-web-course/quizzes/semantic_web_mastery_quiz.html`

## 🛠️ Customization

To customize the website:
1. Edit `index.html` to change content, colors, or layout
2. Update the CSS in the `<style>` section
3. Commit and push changes to GitHub
4. Changes will automatically deploy in 1-2 minutes

## 👨‍🏫 Instructor

**Dr. Radu Mihailescu**  
Associate Professor  
Programme Director MSc AI  
Heriot-Watt University

## 📝 Assessment

- **Class Test**: 20% (Week 7)
- **Final Exam**: 80%
  - Part 1 (40%): Ontologies, OWL, SPARQL, Data Integration
  - Part 2 (40%): NoSQL (covered in weeks 7-11)

## 📧 Support

For questions about course content, please refer to your course materials or contact your instructor.

---

**Built with ❤️ for Big Data Management Students**
