## Activity diagram for Github Pull request

![example_workflow](https://www.plantuml.com/plantuml/img/VLAzJiCm4DxlAMw48P5O4K95WDg53lmyWEjS4wkE7UmpfKAyEoSdX2W4F4Nt_LxiLMGLEBKM0UB1k4u5rMAdz47LzCGdInX8itAr9G2bsGTyYHGkXkz7UZDqf0008m_NXZTfXn-0SZ8RYs3gXWl4izj0YWbtGJdTd6VAR8P5vO-kk9QvRrl3o7w4BXszyo3w1VxeUhykMIlrNnD5dag7IiM2HyQdX0MddhCSKkOzI-cmzMps9_JSK8YIRfosgIBuMplMlz6QEfwXqzKN2LUb87ScwXJZV7LHagjYh_w-Cqcqj9TBMVJx9sai-a2X9h5_tjnlPt-sX_8GFW5M4Y-lx0i0)

```
@startuml 

skinparam packageStyle rectangle

actor User1
actor Reviewer


rectangle GitHub {
    User1 -right-  (Create branch)
    (Create branch) -down-> (Commit to branch) :next
    (Commit to branch) -down-> (Create pull request) :next
    User1 -- (Commit to branch)
     User1 -- (Create pull request)
     (Create pull request) .right.> (Notify others) :include
    (Create pull request) -down-> (Accept pull request)  :next
    (Accept pull request) <.  (Discuss pull request) :extends
    (Reviewer) -left- (Accept pull request)
    (Accept pull request) -down-> (Merge) :next
    User1 -- (Merge)
    
}

@enduml
```


![](https://www.plantuml.com/plantuml/img/VL91JiGm3Bpx5Jx2ePMu8eGMWSHUu03Y0TdKsqQR9iLnM5Q8lnEbfLGba5FacV6Cuso2A9ROMmG81-C6nQh7GUc3QkbPJfQGIOjohIK0fSKplWJYY-d-H6-6ZiG0CFFmtiWsxl03C9tCnefDsqc5U7RBf8HmnyhfxZnJLZMi6dzqrNMg-xutWk9dwDBHkqoYN-2FRkmtH6jJ_DT8GPRIAL9Lw97n9Q7GQUIKJUeyPvqoF7en-nDwwOX3SZTEszWG_AsTuzzeJOEiqENeHS9LdP0x4tGCOJrwKf9hmgZ-tbbojBHFIods-yTf3lf0t5BvPKSe5-4JO9Fiqo_x0W00)

