# Repository "uni_uebungen_mathe"
Material for organization of big exercise classes in math at German universities

# LaTeX part

Ecosystem for typing problem sheets, their solutions and exams.

## Philosophy:

1. A single solution corresponds to a command in `loesungen.tex`. E.g., one defines
   ```
   \newcommand{\BIIILV}{
   1+1=2
   }
   ```
   for the solution of the fifth problem on the third exercise sheet.

2. The file `alle_loesungen.tex` is the main file containing the preamble for subfiles and loading `loesungen.tex`.

3. The file `musterloesung.tex` is a subfile of `alle_loesungen.tex`. When a solution to the third exercise sheetis written, one makes a copy of `musterloesung.tex` to `loesung3.tex` and then fills `loesung3.tex` with the list of corresponding solutions:
   ```
   \BIIILIV
   \BIIILV
   ```
4. One compiles `loesung3.tex` to obtain the pdf with sollutions to the third exercise sheet. One can also include `loesung3.tex` in `alle_loesungen.tex`, e.g.,
   ```
   \subfile{loesung2.tex}
   \subfile{loesung3.tex}
   ```
   to obtain a list of solutions at the end of semester.

5. Similar philosophy applies to exercise sheets and to exams. The exam allows to add points and comments for the correctors which can be shown or hidden. 
   
# Excel part (coming soon)

Excel documents to keep track of points from homeworks and exams and creating statistics.
