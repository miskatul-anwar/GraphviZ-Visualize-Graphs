# Graphviz Examples with Directory Structure
Graphviz is open source graph visualization software. This repository contains a collection of Graphviz source files (`.gv`) and their corresponding output images (`.png`).

## Directory Structure

```
├── LICENSE
├── README.md
├── src  # source code goes here
│   ├── 1.gv
│   ├── 2.gv
│   ├── 3.gv
│   ├── 4.gv
│   ├── 5.gv
│   ├── 6.gv
│   └── 7.gv
└── target # all the outputs
    ├── 01.png
    ├── 02.png
    ├── 03.png
    ├── 04.png
    ├── 05.png
    ├── 06.png
    └── 07.png
```

## Examples

Below are the source codes along with their corresponding outputs:

### Graph 1

**Source (`src/1.gv`):**
```dot
graph G{
  A -- B
}
```

**Output (`target/01.png`):**
![Graph 1](target/01.png)

---

### Graph 2

**Source (`src/2.gv`):**
```dot
digraph G{
  A -> B
  B -> C 
  C -> A
}
```

**Output (`target/02.png`):**
![Graph 2](target/02.png)

---

### Graph 3

**Source (`src/3.gv`):**
```dot
digraph G {
  A -> {B,C,D}
}
```

**Output (`target/03.png`):**
![Graph 3](target/03.png)

---

### Graph 4

**Source (`src/4.gv`):**
```dot
digraph G {
  {A,B,C} -> {D,E,F}
}
```

**Output (`target/04.png`):**
![Graph 4](target/04.png)

---

### Graph 5

**Source (`src/5.gv`):**
```dot
digraph G {
  node [style=filled, color=lightblue]
  {A,B,C} -> {D,E,F}
}
```

**Output (`target/05.png`):**
![Graph 5](target/05.png)

---

### Graph 6

**Source (`src/6.gv`):**
```dot
digraph G {
  node [shape=square,style=filled, color=lightblue]
  edge [style=dotted, color=grey]
  {A,B,C}->{D,E,F}
  B [ shape=triangle,color=grey]
}
```

**Output (`target/06.png`):**
![Graph 6](target/06.png)

---

### Graph 7

**Source (`src/7.gv`):**
```dot
digraph G {
  layout = neato
  node [shape=circle,style=filled, color=lightblue]
  edge [style=dashed, color=grey]
  A-> {B,C,D,E,F,G}
  A [ shape=triangle,color=grey]
}
```

**Output (`target/07.png`):**
![Graph 7](target/07.png)
---

## How to Generate Graphs

To generate PNG files from the Graphviz `.gv` files, use the following command:

```bash
dot -Tpng src/<file.gv> -o target/<output.png>
```

Replace `file.gv` and `output.png` with the appropriate filenames for other graphs.



