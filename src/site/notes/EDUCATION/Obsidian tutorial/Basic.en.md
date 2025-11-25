---
{"dg-publish":true,"permalink":"/education/obsidian-tutorial/basic-en/","noteIcon":"","created":"2025-11-25T18:04:33.314+05:00","updated":"2025-11-25T21:04:43.962+05:00"}
---

# Obsidian Beginner’s Guide (English) – Clean & Visual
> [!warning] Reminder:
> #####  Below syntax examples are given. Some of them should be wrapped with two <b>```</b> backticks when using. They are marked as #InsideTripleBacktics in examples.



<div>![[[[somefile.png\|[[somefile.png]]]]</div>
---
# 001. Install Obsidian in 1 Minute

1. Go to [obsidian.md](https://obsidian.md)
2. Download the installer for your OS (Windows/Mac/Linux)
3. Run the installer → Follow prompts
4. Launch Obsidian → Done! It's free and open-source.



---
# 002. Switch to Uzbek Language Fast

1. Settings → Appearance → Language
2. Select “Uzbek (Ўзбек)”
3. Restart the app → Everything switches to Uzbek.


---
# 003. Create New Note in One Click

1. Press Ctrl + N → New blank note
2. Or click “+” in the left sidebar
3. Name the file right away (supports Latin or Cyrillic).



---
# 004. Headings with Hash Levels


- [ ] *Syntax*:
```code
# H1 Heading (Biggest)
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading (smallest)
```
- [x] *Result*:

# H1 Heading (Biggest)
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading (smallest)



---
# 005. How to Make Text Bold in Obsidian


- [ ] *Syntax*:
```code
**bold** or __bold__
```
- [x] *Result*: 
**bold** or __bold__



---
# 006. How to Write Italic Text Fast


- [ ] *Syntax*:
```code
*italic* or _italic_
```
- [x] *Result*:
*italic* or _italic_




---
# 007. Strikethrough Text Tutorial


- [ ] *Syntax*:
```code
~~strikethrough~~
```
- [x] *Result*:
~~strikethrough~~





---
# 008. Highlight Important Text Easily


- [ ] *Syntax*:
```code
==highlight==
```
- [x] *Result*:






---
# 009. Toolbar Quick Formatting Tips
Select text → use:
- `Ctrl+B` → **bold**
- `Ctrl+I` → *italic*
- `Ctrl+D` → ~~strikethrough~~
- `Alt+H` → ==highlight==





---
# 010. Horizontal Divider Line in Obsidian


- [ ] *Syntax*:
```code
---
***
___
```
- [x] *Result*:
---
***
___




---
# 011. Block Quotes for Better Notes


- [ ] *Syntax*:
```code
> Single level quote
>> Nested quote
```
- [x] *Result*:

> Single level quote
>> Nested quote





---
# 012. Bulleted Lists in Obsidian


- [ ] *Syntax*:
```code
- Item 1
- Item 2
  - Sub-item
```
- [x] *Result*:
- Item 1
- Item 2
  - Sub-item





---
# 013. Numbered Lists Step by Step


- [ ] *Syntax*:
```code
1. First
2. Second
   3. Sub 1
   4. Sub 2
```
- [x] *Result*:
1. First
2. Second
   3. Sub 1
   4. Sub 2





---
# 014. Indent and Outdent Lists
#### `Tab` → indent  
#### `Shift+Tab` → outdent





---
# 015. Task Checkboxes in Obsidian


- [ ] *Syntax*:
```code
- [ ] Not done
- [x] Done
- [>] Deferred
- [?] Question
```
- [x] *Result*:

- [ ] Not done
- [x] Done
- [>] Deferred
- [?] Question





---
# 016. Add External Links Correctly


- [ ] *Syntax*:
```code
[Obsidian](https://obsidian.md)
```
- [x] *Result*: → [Obsidian](https://obsidian.md)





---
# 017. Simple Internal Links Wiki Style


- [ ] *Syntax*:
```code
[[031. Math in Obsidian\|031. Math in Obsidian]]
```
- [x] *Result*: → [[031. Math in Obsidian\|031. Math in Obsidian]]





---
# 018. Aliased Internal Links


- [ ] *Syntax*:
```code
[[031. Math in Obsidian\|LaTeX Guide]]
```
- [x] *Result*: → [LaTeX Guide]([[031. Math in Obsidian\|031. Math in Obsidian]])





---
# 019. Link to Headings Inside Note


- [ ] *Syntax*:
```code
[[Obsidian Guide#005. How to Make Text Bold in Obsidian\|Bold Text]]
```
- [x] *Result*: → [Bold Text]([[Obsidian Guide#005. How to Make Text Bold in Obsidian\|Obsidian Guide#005. How to Make Text Bold in Obsidian]])





---
# 020. Embed Notes with Exclamation


- [ ] *Syntax*:
```code
![[001. Install Obsidian in 1 Minute\|001. Install Obsidian in 1 Minute]]
```
- [x] *Result*: → (embeds the whole note here)

Resize example:  
```code
![[photo.jpg\|300]]
```





---
# 021. Code Blocks and Syntax Highlight


- [ ] *Syntax*:
    ```python
    print("Hello Obsidian!")
    ```
- [x] *Result*:  
```python
print("Hello Obsidian!")
```





---
# 022. Create Tables in Obsidian Fast


- [ ] *Syntax*:
```code
| Name   | Age | City       |
|:-------|:---:|-----------:|
| Ali    | 25  | Tashkent   |
| Vali   | 30  | Samarkand  |
```
- [x] *Result*:

| Name   | Age | City       |
|:-------|:---:|-----------:|
| Ali    | 25  | Tashkent   |
| Vali   | 30  | Samarkand  |





---
# 023. Assets Folder Setup


- [ ] *Syntax*:
Create folder → `Assets` or `Attachments` → drop all media there.





---
# 024. Embed Audio Files in Notes


- [ ] *Syntax*:
```code
![[song.mp3\|song.mp3]]
```
Plays inline.
- [x] *Result*:




---
# 025. Embed Local Video Files Easily


- [ ] *Syntax*:
##### markdown
```code
![[video.mp4\|video.mp4]]
```
##### html 
```code
<video src="local_path_or_external_url_link" width="300" controls></video>
```
- [x] *Result*:
<video src="assets/animated_1.mp4" width="300" controls></video>




---
# 026. Embed PDF Documents in Obsidian


- [ ] *Syntax*:
```code
![[paper.pdf\|paper.pdf]]
![[paper.pdf\|200]]
![[paper.pdf#page=5\|paper.pdf#page=5]]
```
Shows page 5 directly.
- [x] *Result*:
![[progit.pdf|200]]



---
# 027. Add and Embed Images Properly


- [ ] *Syntax*:
```code
![.[photo.jpg].]
![.[photo.jpg|400x300].]
![.[photo.jpg|right|250].]
```
Aligns right with width 250px.
- [x] *Result*:


![EDUCATION/Obsidian tutorial/assets/original_logo.jpg|right|250](/img/user/EDUCATION/Obsidian%20tutorial/assets/original_logo.jpg)


---
# 028. Embed Maps


- [ ] *Syntax*:
```code
<iframe width=600 height=600 src="the_url_of_a_map" />
```

- [x] *Result*:
<iframe width="425" height="350" src="https://www.openstreetmap.org/export/embed.html?bbox=71.52442932128908%2C40.2748109313747%2C71.97761535644533%2C40.51171103483292&amp;layer=mapnik" style="border: 1px solid black"></iframe>

---
# 029. Callouts for Beautiful Notes


- [ ] *Syntax*:
```code
> [!info] Title
> Useful information
```
- [x] *Result*:
> [!info] Title
> Useful information


- [ ] *Syntax*:
```code
> [!tip] Quick Tip
> Save time with this!
```
- [x] *Result*:
> [!tip] Quick Tip
> Save time with this!


- [ ] *Syntax*:
```code
> [!warning] Careful
> This might break something
```
- [x] *Result*:
> [!warning] Careful
> This might break something

Other types: `note`, `abstract`, `success`, `error`, `example`, `quote`





---
# 030. Flowcharts and Diagrams Fast (Mermaid)
#InsideTripleBacktics 

- [ ] *Syntax*:
```code
mermaid
graph TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Good]
    B -->|No| D[Try Again]
```
- [x] *Result*:
```mermaid
graph TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Good]
    B -->|No| D[Try Again]
```





---
# 031. Math in Obsidian | LaTeX
### Inline:  


- [ ] *Syntax*
`$E = mc^2---
{"dg-publish":true,"permalink":"/education/obsidian-tutorial/basic-en/","noteIcon":"","created":"2025-11-25T18:04:33.314+05:00","updated":"2025-11-25T21:04:43.962+05:00"}
---

# Obsidian Beginner’s Guide (English) – Clean & Visual
> [!warning] Reminder:
> #####  Below syntax examples are given. Some of them should be wrapped with two <b>```</b> backticks when using. They are marked as #InsideTripleBacktics in examples.



<div>![[[[somefile.png]]]]</div>
---
# 001. Install Obsidian in 1 Minute

1. Go to [obsidian.md](https://obsidian.md)
2. Download the installer for your OS (Windows/Mac/Linux)
3. Run the installer → Follow prompts
4. Launch Obsidian → Done! It's free and open-source.



---
# 002. Switch to Uzbek Language Fast

1. Settings → Appearance → Language
2. Select “Uzbek (Ўзбек)”
3. Restart the app → Everything switches to Uzbek.


---
# 003. Create New Note in One Click

1. Press Ctrl + N → New blank note
2. Or click “+” in the left sidebar
3. Name the file right away (supports Latin or Cyrillic).



---
# 004. Headings with Hash Levels


- [ ] *Syntax*:
```code
# H1 Heading (Biggest)
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading (smallest)
```
- [x] *Result*:

# H1 Heading (Biggest)
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading (smallest)



---
# 005. How to Make Text Bold in Obsidian


- [ ] *Syntax*:
```code
**bold** or __bold__
```
- [x] *Result*: 
**bold** or __bold__



---
# 006. How to Write Italic Text Fast


- [ ] *Syntax*:
```code
*italic* or _italic_
```
- [x] *Result*:
*italic* or _italic_




---
# 007. Strikethrough Text Tutorial


- [ ] *Syntax*:
```code
~~strikethrough~~
```
- [x] *Result*:
~~strikethrough~~





---
# 008. Highlight Important Text Easily


- [ ] *Syntax*:
```code
==highlight==
```
- [x] *Result*:






---
# 009. Toolbar Quick Formatting Tips
Select text → use:
- `Ctrl+B` → **bold**
- `Ctrl+I` → *italic*
- `Ctrl+D` → ~~strikethrough~~
- `Alt+H` → ==highlight==





---
# 010. Horizontal Divider Line in Obsidian


- [ ] *Syntax*:
```code
---
***
___
```
- [x] *Result*:
---
***
___




---
# 011. Block Quotes for Better Notes


- [ ] *Syntax*:
```code
> Single level quote
>> Nested quote
```
- [x] *Result*:

> Single level quote
>> Nested quote





---
# 012. Bulleted Lists in Obsidian


- [ ] *Syntax*:
```code
- Item 1
- Item 2
  - Sub-item
```
- [x] *Result*:
- Item 1
- Item 2
  - Sub-item





---
# 013. Numbered Lists Step by Step


- [ ] *Syntax*:
```code
1. First
2. Second
   3. Sub 1
   4. Sub 2
```
- [x] *Result*:
1. First
2. Second
   3. Sub 1
   4. Sub 2





---
# 014. Indent and Outdent Lists
#### `Tab` → indent  
#### `Shift+Tab` → outdent





---
# 015. Task Checkboxes in Obsidian


- [ ] *Syntax*:
```code
- [ ] Not done
- [x] Done
- [>] Deferred
- [?] Question
```
- [x] *Result*:

- [ ] Not done
- [x] Done
- [>] Deferred
- [?] Question





---
# 016. Add External Links Correctly


- [ ] *Syntax*:
```code
[Obsidian](https://obsidian.md)
```
- [x] *Result*: → [Obsidian](https://obsidian.md)





---
# 017. Simple Internal Links Wiki Style


- [ ] *Syntax*:
```code
[[031. Math in Obsidian]]
```
- [x] *Result*: → [[031. Math in Obsidian]]





---
# 018. Aliased Internal Links


- [ ] *Syntax*:
```code
[[031. Math in Obsidian|LaTeX Guide]]
```
- [x] *Result*: → [LaTeX Guide]([[031. Math in Obsidian]])





---
# 019. Link to Headings Inside Note


- [ ] *Syntax*:
```code
[[Obsidian Guide#005. How to Make Text Bold in Obsidian|Bold Text]]
```
- [x] *Result*: → [Bold Text]([[Obsidian Guide#005. How to Make Text Bold in Obsidian]])





---
# 020. Embed Notes with Exclamation


- [ ] *Syntax*:
```code
![[001. Install Obsidian in 1 Minute]]
```
- [x] *Result*: → (embeds the whole note here)

Resize example:  
```code
![[photo.jpg|300]]
```





---
# 021. Code Blocks and Syntax Highlight


- [ ] *Syntax*:
    ```python
    print("Hello Obsidian!")
    ```
- [x] *Result*:  
```python
print("Hello Obsidian!")
```





---
# 022. Create Tables in Obsidian Fast


- [ ] *Syntax*:
```code
| Name   | Age | City       |
|:-------|:---:|-----------:|
| Ali    | 25  | Tashkent   |
| Vali   | 30  | Samarkand  |
```
- [x] *Result*:

| Name   | Age | City       |
|:-------|:---:|-----------:|
| Ali    | 25  | Tashkent   |
| Vali   | 30  | Samarkand  |





---
# 023. Assets Folder Setup


- [ ] *Syntax*:
Create folder → `Assets` or `Attachments` → drop all media there.





---
# 024. Embed Audio Files in Notes


- [ ] *Syntax*:
```code
![[song.mp3]]
```
Plays inline.
- [x] *Result*:




---
# 025. Embed Local Video Files Easily


- [ ] *Syntax*:
##### markdown
```code
![[video.mp4]]
```
##### html 
```code
<video src="local_path_or_external_url_link" width="300" controls></video>
```
- [x] *Result*:
<video src="assets/animated_1.mp4" width="300" controls></video>




---
# 026. Embed PDF Documents in Obsidian


- [ ] *Syntax*:
```code
![[paper.pdf]]
![[paper.pdf|200]]
![[paper.pdf#page=5]]
```
Shows page 5 directly.
- [x] *Result*:
![[progit.pdf|200]]



---
# 027. Add and Embed Images Properly


- [ ] *Syntax*:
```code
![.[photo.jpg].]
![.[photo.jpg|400x300].]
![.[photo.jpg|right|250].]
```
Aligns right with width 250px.
- [x] *Result*:


![EDUCATION/Obsidian tutorial/assets/original_logo.jpg|right|250](/img/user/EDUCATION/Obsidian%20tutorial/assets/original_logo.jpg)


---
# 028. Embed Maps


- [ ] *Syntax*:
```code
<iframe width=600 height=600 src="the_url_of_a_map" />
```

- [x] *Result*:
<iframe width="425" height="350" src="https://www.openstreetmap.org/export/embed.html?bbox=71.52442932128908%2C40.2748109313747%2C71.97761535644533%2C40.51171103483292&amp;layer=mapnik" style="border: 1px solid black"></iframe>

---
# 029. Callouts for Beautiful Notes


- [ ] *Syntax*:
```code
> [!info] Title
> Useful information
```
- [x] *Result*:
> [!info] Title
> Useful information


- [ ] *Syntax*:
```code
> [!tip] Quick Tip
> Save time with this!
```
- [x] *Result*:
> [!tip] Quick Tip
> Save time with this!


- [ ] *Syntax*:
```code
> [!warning] Careful
> This might break something
```
- [x] *Result*:
> [!warning] Careful
> This might break something

Other types: `note`, `abstract`, `success`, `error`, `example`, `quote`





---
# 030. Flowcharts and Diagrams Fast (Mermaid)
#InsideTripleBacktics 

- [ ] *Syntax*:
```code
mermaid
graph TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Good]
    B -->|No| D[Try Again]
```
- [x] *Result*:
```mermaid
graph TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Good]
    B -->|No| D[Try Again]

- [x] *Result*:
$E = mc^2$

### Block:  


- [ ] *Syntax*
```code
$$
\int_0^\infty e^{-x^2} \, dx = \frac{\sqrt{\pi}}{2}
$$
```
- [x] *Result*:
$$
\int_0^\infty e^{-x^2} \, dx = \frac{\sqrt{\pi}}{2}
$$

## You’ve mastered Obsidian basics!  
Next step: enable Core Plugins → Graph View, Daily Notes, and explore Community Plugins. Happy note-taking! 🚀