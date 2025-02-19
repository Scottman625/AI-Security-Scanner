# 🛡️ AI Security Scanner (GitHub Actions)

✅ **使用 OpenAI API 自動檢測代碼中的安全漏洞！**

## 🚀 使用方式
```yaml
name: Security Scan
on: [pull_request, push]

jobs:
  security_check:
    runs-on: ubuntu-latest
    permissions:
      security-events: write

    steps:
      - name: 使用 AI Security Scanner 進行安全掃描
        uses: scottman625/security-scanner-action@v1
        with:
          open_ai_key: ${{ secrets.OPEN_AI_KEY }}  # 用戶提供自己的 OpenAI API Key
          target_branch: "develop"
