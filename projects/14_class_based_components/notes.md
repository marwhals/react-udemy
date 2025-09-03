# Class components lifecyle

---

- Side Effects in Functional componetns useEffect()
  - Class based componets can't use Hooks!

---

- `componentDidMount()` - called once a component mounted --> evaluated and rendered by React --- equivalent to useEffect()
- `componentDidUpdate()` - called once a component updated --> re-evaluated and re-rendered by React -- 
- `componenentWillUnmount()` - Called rigth before a component is unmounted ----> right before removed from DOM ----

---

- Don't have to use Functional Components - You can use class-based components if you prefer them. (No really recommended).

---

## Error Boundary

- Used to catch errors - no functional equivalent.