# Scenarion Based Training

## 🧠 14. Scenario-Based Questions

### 96. How to test login page?

- Validate with **valid and invalid credentials** (correct/incorrect username & password combinations)  
- Check **boundary inputs** (min/max length, empty fields, long strings)  
- Verify **security aspects**:
  - Password masking  
  - SQL injection  
  - Brute force protection (account lockout)  
  - HTTPS usage  

---

### 97. How to design test cases for search?

- Test with **valid inputs** (existing data)  
- Test with **invalid inputs** (non-existing data)  
- Verify behavior for **empty input** (should show message or default results)  
- Check **special characters and symbols**  
- Validate **case sensitivity and partial matches**  

---

### 98. How to test dropdown?

- Verify **all values are present and correct**  
- Check **default selected value**  
- Ensure selection works properly  
- Validate **disabled/hidden options (if any)**  

---

### 99. How to test form?

- Validate **mandatory fields** (required field validation)  
- Verify **error messages** are correct and user-friendly  
- Check **data format validation** (email, phone, etc.)  
- Test form submission with valid and invalid inputs  

---

### 100. How to test pagination?

- Verify **Next/Previous buttons functionality**  
- Check **first and last page boundaries**  
- Validate correct number of records per page  
- Ensure no duplicate or missing records  

---

## 🎯 15. Edge & Interview-Tricky Questions

### 101. What is difference between error, defect, failure?

- **Error** → Human mistake while coding or designing  
- **Defect** → Issue found in the application due to error  
- **Failure** → When the system behaves incorrectly during execution  

---

### 102. What is Test Coverage?

It is the **percentage of application (requirements/code)** that is tested using test cases. Higher coverage improves confidence but does not guarantee quality.

---

### 103. Can 100% coverage ensure no bugs?

No. Even with full coverage:

- Edge cases may be missed  
- Logical issues may exist  
- Real-world scenarios may differ  

---

### 104. What is Shift Left Testing?

Testing is performed **early in SDLC**, starting from requirement and design phase to catch defects sooner and reduce cost.

---

### 105. What is Shift Right Testing?

Testing in **production or near-production environments**, focusing on:

- Monitoring  
- Real user behavior  
- Performance and reliability  

---

## 🧾 16. Real-World Understanding

### 106. Why testing is important?

- Ensures **software quality and reliability**  
- Prevents **production failures**  
- Improves **user experience**  
- Reduces long-term cost  

---

### 107. When to stop testing?

- Project deadline reached  
- No critical/high severity bugs remain  
- Test coverage is sufficient  
- Risk is acceptable  

---

### 108. What if requirements are unclear?

- Communicate with **stakeholders or product owner**  
- Ask questions and clarify assumptions  
- Create **test scenarios based on understanding**  
- Document ambiguities  

---

### 109. How to handle changing requirements?

- Follow **Agile methodology**  
- Update test cases regularly  
- Prioritize regression testing  
- Maintain flexibility in test design  

---

### 110. What is risk in testing?

Risk is a **potential problem area** that may cause failure. It is identified based on:

- Complexity  
- Business impact  
- Past defects  

---

## 🧠 17. Extra Deep Concepts

### 111. What is Test Oracle?

A mechanism used to determine the **expected result** of a test case for comparison with actual output.

---

### 112. What is Static Testing?

Testing performed **without executing the code**, such as:

- Code reviews  
- Requirement analysis  
- Walkthroughs  

---

### 113. What is Dynamic Testing?

Testing performed **by executing the application**, validating actual behavior.

---

### 114. What is Alpha Testing?

Testing performed internally by the **development/testing team** before releasing to users.

---

### 115. What is Beta Testing?

Testing performed by **real users in real environments** before final release.

---

## 🔥 18. Expert-Level Questions

### 116. How do you ensure maximum coverage?

- Use **RTM (Requirement Traceability Matrix)**  
- Apply test design techniques (BVA, EP, etc.)  
- Cover all positive, negative, and edge cases  

---

### 117. How to reduce test cases but keep coverage?

- Use **Equivalence Partitioning** to group inputs  
- Remove duplicate scenarios  
- Focus on high-risk areas  

---

### 118. What is defect leakage?

When a **bug is missed during testing** and found in production.

---

### 119. What is defect density?

Number of defects per module or lines of code, used to measure **software quality**.

---

### 120. What is test effectiveness?

It measures how effectively testing identifies defects:

- High effectiveness → more bugs caught before release  
- Calculated as: **(Defects found in testing / Total defects)**
