# DeepLabCut
## Repogitory
https://github.com/DeepLabCut/DeepLabCut

## Issue
- [鯖落ち](http://deeplabcut.rowland.harvard.edu/)
  - https://github.com/DeepLabCut/DeepLabCut/issues/2057
  - https://github.com/DeepLabCut/DeepLabCut/pull/2059
- Stable版 (v2.2.3)はharvard.eduからモデルやweightsをDLして来るため使えない
- v2.3rc3はHugging Faceを利用

## Installation
- Issueより、Stable版を利用すると404が出るため、最新版のv2.3rc3を利用
- 公式推奨方法はどれもLinuxで動かなかったので以下に手順を記載
  - conda: pipエラー
  - pip: import時エラー
  - docker: Stable版で鯖落ちのため利用不可

```
1. DeepLabCut/conda-environments/DEEPLABCUT.yamlを編集
  - guiでコケるので、"deeplabcut[tf]"に変更
  - https://github.com/DeepLabCut/DeepLabCut/issues/2044

2. conda env create -f DEEPLABCUT.yaml
  - これでStable版(v2.2.3)がインストールされる

3. ./reinstall.sh
  - 最新版 (v2.3rc3)にアップデート

4. import deeplabcut
  - 何個か足りないライブラリがあり怒られるのでインストール
```
