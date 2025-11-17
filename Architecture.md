# Reasons for moving code out of larger codebases, by decade (1990s–2020s)
*Cultural, practical, conceptual, and technological motivations that influenced real-world codebases.*

---

# **1990s — The Encapsulation & Component Era**

### **1. Encapsulation and Information Hiding (OOP influence)**

Motivation:

* reduce accidental coupling
* hide private data
* enforce interfaces
* keep each class “clean”

Reason:

> “Put this in another file because OOP says so.”

### **2. GUI vs Logic separation**

Motivation:

* structure between UI code and business logic
* avoid logic inside event handlers

Reason:

> “Move logic to its own unit/file so the UI stays readable.”

### **3. Reusability / Libraries**

Motivation:

* create static libraries (.lib, .a) and DLLs/.so
* reuse in several programs

Reason:

> “Extract so multiple programs can use it without copying.”

### **4. Vendor/API integration**

Motivation:

* wrap Windows API, Unix API, or 3rd-party libraries

Reason:

> “Don’t clutter the main program with API glue.”

---

# **2000s — The Framework & Layering Era**

### **1. Layered Architecture (N-tier design)**

Motivation:

* separate database, business logic, UI
* enforce clean layering (DAL, BLL, UI)

Reason:

> “Move this to the ‘BLL’ layer because that’s the diagram.”

### **2. MVC/MVP patterns**

Motivation:

* isolate presentation logic
* avoid fat controllers or "God classes"

Reason:
> “Move this logic into a model or presenter.”

### **3. Testability**

Motivation:

* extract code so it can be unit tested
* separate pure logic from side effects

Reason:

> “Move this so we can write tests for it.”

### **4. XML/SOAP service wrappers**

Motivation:

* isolate service calls and DTOs

Reason:

> “Put this in a service client module so everything is uniform.”

---

# **2010s — The Microservice & Dependency Explosion Era**

### **1. Microservices / modular deployment**

Motivation:

* each service in its own repo or module
* independent deployment and scaling

Reason:

> “Split code so different teams can deploy separately.”

### **2. Dependency-Driven Structure**

Motivation:

* npm, pip, NuGet culture
* using packages for trivial tasks (left-pad phenomenon)

Reason:

> “Move this code into a module because that’s how the package ecosystem works.”

### **3. Code Organization Around Data Models**

Motivation:

* DDD (Domain-Driven Design)
* entities, aggregates, value objects

Reason:

> “Extract because it belongs to this bounded context.”

### **4. Avoiding God Classes by Sharding**

Motivation:

* break giant files into multiple, smaller ones

Reason:

> “The file is too large; split by topic.”

---

# **2020s — The Cloud, Tooling, and Maintainability Era**

### **1. Tooling Pressure (IDE, linters, static analyzers)**

Motivation:

* IDEs work better with smaller modules
* code linters encourage splitting by “responsibility”

Reason:

> “Move to another file because the linter complains.”

### **2. DevOps pipelines**

Motivation:

* different modules built/tested in separate stages
* partial builds to speed CI/CD

Reason:

> “Extract to reduce build times and pipeline steps.”

### **3. API-first / contract-first development**

Motivation:

* generate modules from API definitions
* keep API client code separate

Reason:

> “Generated code goes in its own unit.”

### **4. Type Systems & Language Features**

Motivation:

* languages with enforced modules (Go, Rust)
* namespacing by file structure

Reason:

> “Compiler/language enforces extraction.”

### **5. Cognitive Load Reduction**

Motivation:

* break big files into smaller bite-sized modules
* reduce mental overhead

Reason:

> “This file is too big for comfort; split something out.”

---

# **Summary:**

Historical reasons (1990s–2020s) revolve around:

* responsibility grouping
* reuse
* readability
* testability (required by Crash-Fast)
* deployment
* "tech stack" (framework of the day)
* team structure (for orgs)
* evolving language/IDE limitations and fashions

**None** revolve around:

> **“Extract code because it is finished, stable, deterministic, and will not change again in a reasonable without providing backwards compatibility”**

Pretty much all of these look like weak motivations, in hindsight. We have been adopting to the motivation of the day.

API-first / contract-first motivation is always valid (for interfaces), and **do wrap** third-party interfaces. **But...**

# If no architectures are about the code, which architecture *does*?
*to be continued...* ;)


Or anything else.
