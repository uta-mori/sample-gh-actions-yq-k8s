# 参考

- [GitHub Actions で真偽値を正しく扱う ｜ loop.run_forever()](https://note.sarisia.cc/entry/boolean-in-github-actions/)
- [Github Actionsでrepository dispatch eventを使用して外部からActionsを実行するメモ | 7me](https://7me.nobiki.com/2020/11/30/github-actions-repository-dispatch-event-api/)


# テスト

```bash

// コマンド履歴を残さないようにする(A)
$ HISTIGNORE=*

// GithubのParsonal Access Tokenをセットする
$ export TOKEN=xxxxxxxxxxxxxxxxxxx

// (A)の解除
$ unset HISTIGNORE

$ curl -X POST -H "Authorization: token $TOKEN" -H "Accept: application/vnd.github.everest-preview+json" --data '{"event_type": "apple","reviewer":"you", "auto": true }' https://api.github.com/repos.uta-mori/sample-gh-actions-yq-k8s/dispatches

```