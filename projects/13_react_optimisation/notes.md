# React optimisation techniques

---

- The relation between components is internally modelled as a tree structure

---

--> See React developer tools

---

- Using memo
  - Use it as high up in the component tree as possible
    - Blocking a component execution, there will also block all child component executions.
  - Checking props with memo() costs performance
    - Don't wrap it around all your components, it will just add a lot unnecessary checks
  - Don't use it on components where props will change frequently
    - memo() would perform a meaningless check in such cases (which costs performance)

---

- React checks for necessary DOM updates via a "virtual DOM"
  - It creates and compares virtual DOM snapshots to find out which parts of the rendered UI need to be updated

---

## MillionJS 

- Used to speed up react by changing the way react interacts with the virtual DOM