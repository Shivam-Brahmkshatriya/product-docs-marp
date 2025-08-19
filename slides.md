---
marp: true
theme: custom
paginate: true
header: "Product Documentation"
footer: "23ds3000034@ds.study.iitm.ac.in"
---

<!-- _class: lead -->
# 🚀 Product Documentation with Marp  
23ds3000034@ds.study.iitm.ac.in

---

## Why Marp?

- Write once in Markdown  
- Version control friendly (Git)  
- Export to **HTML / PDF / PPTX**  
- Perfect for technical documentation

---

## Custom Theme Example

This slide is styled with **custom CSS** defined in `custom-theme.css`.

- Blue headers  
- Pink sub‑headers  
- Dark code blocks with Fira Code font  

---

## Background Image

![bg left:40%](./images/product-diagram.png)

- Clean product diagram on the left  
- Key bullet points on the right  

---

## Algorithm Complexity

We analyze runtime using **Big‑O notation**:

- $O(n \log n)$ best‑case (e.g., merge sort)  
- $O(n^2)$ worst‑case (e.g., bubble sort)  

---

## Example Code

def quicksort(arr):
if len(arr) <= 1:
return arr
pivot = arr[len(arr)//2]
left = [x for x in arr if x < pivot]
mid = [x for x in arr if x == pivot]
right = [x for x in arr if x > pivot]
return quicksort(left) + mid + quicksort(right)


---

# ✅ Thank You
## Questions?  
23ds3000034@ds.study.iitm.ac.in
