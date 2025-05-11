# Database-SQL

# 高校人事管理系统

## 📌 项目简介
本项目是一个基于 PHP + MySQL 实现的高校人事档案管理系统，用于管理在职人员、退休人员、临时工等基础信息。项目涵盖了数据的增删改查、统计分析与排序展示，模拟真实人事系统的数据维护流程。

## 🧰 使用技术
- 后端语言：PHP
- 数据库：MySQL 5.7
- 开发环境：WampServer（Windows + Apache + MySQL + PHP）
- 数据管理工具：phpMyAdmin
- 编辑器：CodeLobster PHP Edition

## 💡 核心功能模块
1. **数据添加**：表单填写信息后通过 `INSERT INTO` 写入数据库。
2. **数据删除**：支持通过 `id` 删除指定记录。
3. **数据修改**：基于主键更新对应记录字段。
4. **数据查询**：通过 `id` 精确匹配或姓名模糊查询。
5. **数据统计**：如统计在职人数、党员人数、高学历/高职称人数等，使用 `COUNT(*)` 实现。
6. **排序展示**：按照年龄或来院时间升序排序输出数据。
7. **界面支持**：基于 HTML + PHP 构建网页交互界面，适配多功能按钮操作。

## 🗃️ 数据表结构（emp_info）
| 字段名 | 类型 | 说明 |
|--------|------|------|
| id | INT | 员工编号（主键） |
| name | VARCHAR | 姓名 |
| sex | VARCHAR | 性别 |
| age | INT | 年龄 |
| position | VARCHAR | 职务 |
| title | VARCHAR | 职称 |
| p_sta | VARCHAR | 政治面貌 |
| h_edu | VARCHAR | 最高学历 |
| period | INT | 任职时间（单位：年） |
| first_time | DATE | 来院时间 |
| type | VARCHAR | 人员类别 |

## 📊 示例 SQL 语句
```sql
-- 查询党员人数及其信息
SELECT * FROM emp_info WHERE p_sta='党员';
SELECT COUNT(*) FROM emp_info WHERE p_sta='党员';

-- 插入新员工
INSERT INTO emp_info VALUES (15, '张三', '男', 35, '讲师', '副教授', '群众', '硕士', 5, '2018-09-01', '在职人员');

-- 按年龄排序
SELECT * FROM emp_info ORDER BY age ASC;
```

## 📷 截图说明
项目支持通过网页进行数据管理操作，相关截图请见原始报告文档或另附 PDF 说明。

## 🧠 项目收获
通过该项目，掌握了 MySQL 数据库设计、SQL 增删改查操作、PHP 后端开发与前端交互等技能，为后续数据分析与数据库应用开发打下坚实基础。

---
