# LK

**测试工程师 · 求职中**

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![pytest](https://img.shields.io/badge/pytest-8.3.4-green)
![Postman](https://img.shields.io/badge/Postman-API%20Testing-orange)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115.6-009688)

专注**接口自动化测试**与**测试用例设计**，能独立搭建被测系统并完成全链路测试。
下面两个项目覆盖了接口测试、异常与边界场景、数据库校验、缺陷定位与持续集成。

---

## 📌 项目一 · 接口自动化测试框架

### [conduit-api-test](https://github.com/XMSSY123/conduit-api-test)
[![API Automation Tests](https://github.com/XMSSY123/conduit-api-test/actions/workflows/api-test.yml/badge.svg)](https://github.com/XMSSY123/conduit-api-test/actions/workflows/api-test.yml)
![用例](https://img.shields.io/badge/用例-34%20条-informational)
![缺陷](https://img.shields.io/badge/发现缺陷-3%20个-critical)

对开源示范项目 **RealWorld Conduit** 线上 API 的纯黑盒接口自动化测试，不接触服务端源码。

| 亮点 | 说明 |
|---|---|
| 框架分层 | 配置层 / 公共工具层 / 接口封装层 / 用例层，接口变更只改一层 |
| 四层断言 | HTTP 状态码 → 业务状态码 → 关键字段值 → 响应结构 Schema |
| 数据驱动 | PyYAML 管理测试数据，新增用例不改 Python 代码 |
| 用例分级 | smoke / regression / negative / known_bug 四类 marker |
| 资源管理 | fixture 分层（session / function），token 复用 + 数据自动清理 |
| 持续集成 | GitHub Actions 每日定时回归，结果与 Allure 数据自动归档 |

**发现缺陷**：重复点赞导致计数累加（可被单人刷高）、两处错误处理返回 500 并泄露服务端技术栈。
完整缺陷报告 → [DEFECTS.md](https://github.com/XMSSY123/conduit-api-test/blob/main/DEFECTS.md)

---

## 📌 项目二 · 自研系统 + 全链路测试

### [library-system](https://github.com/XMSSY123/library-system)
[![Tests](https://github.com/XMSSY123/library-system/actions/workflows/test.yml/badge.svg)](https://github.com/XMSSY123/library-system/actions/workflows/test.yml)
![用例](https://img.shields.io/badge/设计用例-98%20条-informational)
![缺陷](https://img.shields.io/badge/发现缺陷-3%20个-critical)

独立开发的 **FastAPI + SQLite** 图书借阅管理系统，并对其完成测试用例设计、接口自动化与数据库校验。

| 亮点 | 说明 |
|---|---|
| 用例设计 | 98 条用例设计文档，运用等价类划分、边界值分析、场景法、错误推测 |
| 接口自动化 | 28 条自动化用例，覆盖借还书主流程、库存规则、借阅上限、逾期计费 |
| **数据库校验** | 直接查库验证接口返回与实际落库数据是否一致，纯接口测试看不到的问题也能查出 |
| 测试造数 | 借期固定 30 天，通过改数据库字段构造逾期场景，不用真等 30 天 |
| 缺陷定位 | 结合服务端堆栈与 SQL 语句定位根因，区分业务异常与服务端异常 |

**发现缺陷**：逾期计费边界值 off-by-one 多算一天、还书未恢复库存（接口返回正常，只有查库能发现）、
存在借阅记录时删除图书返回 500。
完整缺陷报告 → [DEFECTS.md](https://github.com/XMSSY123/library-system/blob/main/DEFECTS.md)

---

## 🧰 能力覆盖

| 测试类型 | 项目一 | 项目二 |
|---|---|---|
| 接口功能测试 | ✅ 34 条 | ✅ 28 条自动化 + 98 条设计 |
| 异常 / 边界场景 | ✅ 数据驱动 | ✅ 边界值分析 |
| 权限与越权测试 | ✅ 未授权、越权删除 | ✅ 状态流转拦截 |
| 响应结构校验 | ✅ Schema 校验 | ✅ Pydantic 强类型 |
| 数据库校验 | — | ✅ 接口与数据库交叉验证 |
| 持续集成 | ✅ GitHub Actions | ✅ GitHub Actions |
| 测试报告 | ✅ Allure | ✅ pytest |

**工具栈**：Python · pytest · requests · Allure · Postman · PyYAML · SQLAlchemy · MySQL · Linux · Git

---

## 📫 联系

- GitHub：https://github.com/XMSSY123
- 邮箱：（请填写）

> 完整版简历可联系我获取。
