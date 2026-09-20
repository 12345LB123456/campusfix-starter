# CampusFix 6组版
本仓库用于《基础开发与操作》课程项目。

《基础开发与操作》课程贯穿项目。面向零工程经验学生的 Flask + SQLite 最小 Web 应用，用于练习 Git、协作、测试、CI、Docker 与部署。
到此一游
## 功能范围（起始版本）
- 工单列表、创建工单、查看详情
- SQLite 数据库 + 演示数据（全部虚构）
- `/health` 健康检查接口
- 基本日志配置
- 示例测试（含 1 个故意失败的测试，用于教学）
- `.gitignore`、`.env.example`、README 骨架
## 教学用 Backlog
1. `pytest` 中有一个与“创建工单”相关的失败测试。先复现并记录现象，后续按 Issue → 分支 → PR → Review 流程定位和修复。
2. 创建工单表单的输入校验尚不完整，后续通过测试驱动方式完善。
3. 工单无优先级、无状态流转，可作为小组增量开发 Backlog。
> 学生提示：失败测试是实验素材，不是安装错误。请保留原始失败输出；教师版材料另含根因与参考修复，学生仓库不提前公布答案。
## 运行方法（Windows PowerShell / Ubuntu Bash）
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# Ubuntu:  source .venv/bin/activate
pip install -r requirements.txt
python init_db.py        # 初始化数据库和演示数据
python app.py            # 启动 Flask，访问 http://127.0.0.1:5000
