# Object Oriented Programming (Java Context)

---

## 🧩 10. OOP Concepts (Automation Focus)

### 76. What is OOP?

OOP (Object-Oriented Programming) is a programming paradigm where software is designed using **objects and classes**.  
In Java, everything revolves around classes and objects to improve **modularity, reusability, and maintainability**.

---

### 77. Four pillars of OOP?

- Encapsulation  
- Inheritance  
- Polymorphism  
- Abstraction  

---

### 78. What is Encapsulation?

Encapsulation is the process of **binding data (variables) and methods (functions)** together inside a class and restricting access using access modifiers.

👉 In Java:

- Use `private` variables  
- Provide access via getters/setters  

---

### 79. Example?

```java
public class User {
    private String username;

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }
}
```

### 80. What is Inheritance?

Inheritance allows a child class to reuse properties and methods of a parent class using `extends`.

```java
public class BaseTest {
    public void setup() {
        System.out.println("Browser setup");
    }
}

public class LoginTest extends BaseTest {
    public void testLogin() {
        setup();
    }
}
```

### 81. Types of Inheritance?

- Single  
- Multilevel  
- Hierarchical  

⚠️ Java does not support multiple inheritance with classes (only via interfaces).

### 82. What is Polymorphism?

Polymorphism means one method behaves differently based on context.

---

### 83. Types of Polymorphism?

- Compile-time (Method Overloading)  
- Runtime (Method Overriding)  

---

### 84. What is Method Overloading?

Same method name with different parameters.

```java
public void login(String user) {}
public void login(String user, String password) {}
```

### 85. What is Method Overriding?

Child class provides its own implementation of a parent method.

```java
class BasePage {
    void open() {
        System.out.println("Open base page");
    }
}

class LoginPage extends BasePage {
    @Override
    void open() {
        System.out.println("Open login page");
    }
}
```

### 86. What is Abstraction?

Abstraction means hiding implementation details and exposing only required functionality.

---

### 87. Abstract Class?

- Cannot be instantiated  
- Can have abstract and concrete methods  

```java
abstract class BasePage {
    abstract void loadPage();

    void commonMethod() {
        System.out.println("Common logic");
    }
}
```

### 88. Interface?

- Contains method declarations  
- Supports multiple inheritance  

```java
interface Browser {
    void launch();
}
```

### 89. Abstract Class vs Interface?

- **Abstract Class**
  - Supports **partial implementation**
  - Can have both **abstract and concrete methods**
  - A class **extends** an abstract class

- **Interface**
  - Provides **full abstraction (mostly)**
  - Contains only **method declarations** (default/static methods allowed in modern languages)
  - A class **implements** an interface

---

### 90. Why Interfaces in Automation?

- Enables **loose coupling**
- Supports **multiple browser execution**
- Easy to **switch implementations** (e.g., Chrome, Firefox, Edge)

## 🧱 13. OOP in Automation Framework

### 91. Why OOP Important in Automation?

- **Reusable code**
- **Maintainable framework**
- **Scalable architecture**

---

### 92. Example of Encapsulation in POM?

- **Private locators**
- **Public action methods**

```java
public class LoginPage {

    private By username = By.id("username");

    public void enterUsername(WebDriver driver, String user) {
        driver.findElement(username).sendKeys(user);
    }
}
```

### 93. Inheritance Usage?

- Used to create a **base test class** for common setup and teardown
- Promotes **code reuse** across test classes

```java
public class BaseTest {
    WebDriver driver;

    public void setup() {
        driver = new ChromeDriver();
    }
}
```

### 94. Polymorphism Usage?

- Enables **cross-browser execution**
- Same reference (`WebDriver`) can point to different browser implementations

```java
WebDriver driver;

if(browser.equals("chrome"))
    driver = new ChromeDriver();
else
    driver = new FirefoxDriver();
```

### 95. Abstraction Usage?

Framework layers:

- Test Layer  
- Page Layer  
- Utility Layer  

👉 Test calls page methods, page hides implementation details.
