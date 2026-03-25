\# 表结构设计



\## 学生表（student）



| 字段名       | 数据类型      | 约束                 | 说明     |

|-------------|--------------|----------------------|----------|

| student\_id  | VARCHAR(20)  | PRIMARY KEY          | 学号     |

| student\_name| VARCHAR(50)  |                      | 姓名     |

| gender      | CHAR(2)      |                      | 性别     |

| age         | INT          |                      | 年龄     |


## 课程表（course）

| 字段名       | 数据类型      | 约束                  | 说明         |
|-------------|--------------|-----------------------|--------------|
| course_id   | VARCHAR(20)  | PRIMARY KEY, NOT NULL | 课程号       |
| course_name | VARCHAR(100) | NOT NULL              | 课程名称     |
| credit      | DECIMAL(3,1) | NOT NULL              | 学分         |
| class_hour  | INT          | NOT NULL              | 学时         |
| course_type | VARCHAR(30)  |                       | 课程类型     |
| department  | VARCHAR(50)  |                       | 开课院系     |

### 设计说明
1. `course_id` 作为课程表主键，用来唯一标识一门课程。
2. `course_name` 设为非空，保证课程名称不能为空。
3. `credit` 使用 `DECIMAL(3,1)`，方便保存 2.0、2.5、3.0 这类学分。
4. `class_hour` 使用 `INT`，表示课程总学时。
5. `course_type` 和 `department` 用于补充课程分类信息。


