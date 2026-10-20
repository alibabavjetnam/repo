# az-system — Hệ thống AI agent code ứng dụng

1 orchestrator + 14 agent, 83 skill.

## Cài đặt (Claude Code)
1. Chép thư mục `.claude/` và file `CLAUDE.md` vào thư mục gốc dự án.
2. Thêm `.az/` vào `.gitignore` nếu không muốn commit file trao đổi giữa agent.
3. Mở Claude Code tại thư mục dự án và giao việc bình thường, ví dụ:
   - "Tạo ứng dụng ... " → Luồng A
   - "Fix lỗi ... trong app này" → Luồng B

Lưu ý: subagent trong Claude Code không gọi được subagent khác, nên `saz-orchestrator` chạy ở phiên chính (do `CLAUDE.md` chỉ định); file `saz-orchestrator.md` vẫn được giữ làm định nghĩa vai trò.

## Quy ước tên
- Orchestrator: `saz-orchestrator`
- Agent: `az-<tên>`
- Skill: `z-<tên agent>-<tên skill>`

## Agent và số skill
| Agent | Số skill |
|---|---|
| `saz-orchestrator` | 7 |
| `az-analyst` | 5 |
| `az-explorer` | 7 |
| `az-architect` | 6 |
| `az-frontend` | 5 |
| `az-backend` | 6 |
| `az-database` | 5 |
| `az-debugger` | 6 |
| `az-refactor` | 5 |
| `az-tester` | 7 |
| `az-reviewer` | 5 |
| `az-security` | 5 |
| `az-performance` | 4 |
| `az-devops` | 6 |
| `az-docs` | 4 |
