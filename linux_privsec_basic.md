# Linux Privilege Escalation - Notes

## 📝 今日やったこと
- SUIDファイルの確認方法を覚えた
- `find / -perm -u=s -type f 2>/dev/null` を使って権限昇格に使えるバイナリを調べた

## 🔍 わかったこと
- root権限で実行されるファイルは、悪用できる可能性がある
- GTFOBins というサイトで悪用可能コマンドを調べられる

## 💡 解けなかったところ / 引っかかったところ
- `/usr/bin/python3` のSUIDがある時の使い方が最初わからなかった

## ✔ 解決方法
- GTFOBinsで `python` を調べて、`os.system("/bin/sh")` の例をそのまま使った

## 🚀 次にやること
- 権限昇格の別パターン（Capabilities / PATH悪用 / Cron Job悪用）を触る
