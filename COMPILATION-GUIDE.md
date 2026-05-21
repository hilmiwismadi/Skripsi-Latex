# 📚 NovaTrix Thesis - Compilation Guide

## ✅ Files Ready
- ✓ `main-novatrix.tex` - Main compilation file
- ✓ `contents/chapter-1/chapter-1-novatrix.tex` - Bab 1 (Pendahuluan)
- ✓ `contents/chapter-2/chapter-2-novatrix.tex` - Bab 2 (Tinjauan Pustaka)
- ✓ `references.bib` - Bibliography (updated with NovaTrix references)
- ✓ `compile-novatrix.bat` - Automated compilation script

---

## 🚀 Method 1: Using VS Code LaTeX Workshop (RECOMMENDED)

Since you have **LaTeX Workshop extension** installed:

### Step-by-Step:
1. **Open** `main-novatrix.tex` in VS Code (already opened)
2. **Build** the document:
   - Press `Ctrl+Alt+B` OR
   - Press `Ctrl+S` (auto-build on save) OR
   - Click TEX icon on left sidebar → "Build LaTeX project"
3. **View PDF**:
   - Press `Ctrl+Alt+V` OR
   - Click TEX icon → "View LaTeX PDF"

### If Build Fails:
- Check **Problems panel** (`Ctrl+Shift+M`)
- Check **Output panel** → Select "LaTeX Compiler" from dropdown
- Look for missing packages (MiKTeX should auto-install them)

---

## 🚀 Method 2: Using Batch Script

### Quick Compile:
```cmd
# Double-click this file:
compile-novatrix.bat
```

Or from PowerShell:
```powershell
cd "d:\Hilmi\Coding\MasterFolderSkripsi\Makalah\template_thesis_latex_dteti"
.\compile-novatrix.bat
```

This will:
1. Run pdflatex (3 times)
2. Run bibtex
3. Open the PDF automatically

---

## 🚀 Method 3: Manual Compilation

```powershell
cd "d:\Hilmi\Coding\MasterFolderSkripsi\Makalah\template_thesis_latex_dteti"

pdflatex main-novatrix.tex
bibtex main-novatrix
pdflatex main-novatrix.tex
pdflatex main-novatrix.tex

# Open PDF
start main-novatrix.pdf
```

---

## 🔧 Known Issues & Solutions

### Issue: "File not found" errors
**Solution**: Make sure you're in the correct directory and all chapter files exist

### Issue: Missing packages
**Solution**: MiKTeX will prompt to install them automatically - click "Install"

### Issue: Bibliography not showing
**Solution**: Make sure to run bibtex, then pdflatex twice more

### Issue: Hanging during compilation
**Solution**: 
- Use `-interaction=nonstopmode` flag
- Or press `X` then `Enter` to skip errors
- Check .log file for specific errors

---

## 📄 Output Files

After successful compilation:
- `main-novatrix.pdf` - Your thesis PDF ✅
- `main-novatrix.log` - Compilation log (check for warnings)
- `main-novatrix.aux` - Auxiliary file
- `main-novatrix.bbl` - Bibliography data
- Various other temp files (can be deleted)

---

## ✏️ Before Final Compilation

Update placeholders in `main-novatrix.tex`:
```latex
\program{Teknologi Informasi}{<<Program Coordinator>>}{<<NIP>>}
\departmenthead{<<Head of the Department>>}{<<NIP>>}
\examdate{<<Exam Date>>}
\addsupervisor{<<Dosen Pembimbing 1, S.T., M.Eng., Ph.D.>>}{<<NIP>>}
\addsupervisor{<<Dosen Pembimbing 2, S.T., M.Eng., Ph.D.>>}{<<NIP>>}
```

---

## 📊 What's Inside

### Chapter 1 - Pendahuluan
- Latar Belakang (5 paragraphs with comparison table)
- Rumusan Masalah (3 research questions)
- Tujuan Penelitian (5 objectives)
- Batasan Penelitian (8 constraints)
- Manfaat Penelitian (academic + practical)

### Chapter 2 - Tinjauan Pustaka dan Dasar Teori
- Literature review of LLM/RAG in compliance
- 9 theoretical foundations (ISO 27001, ISMS, SoA, RAG, LLM, etc.)

---

## 🎯 Next Steps

1. ✅ Compile the thesis
2. ✅ Review the PDF output
3. ✏️ Update placeholder information
4. 📝 Add remaining chapters (3, 4, 5, 6) as needed
5. 🔍 Proofread content
6. 📚 Verify all citations

---

**Happy Writing! 🎓**
