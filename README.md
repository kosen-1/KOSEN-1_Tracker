# KOSEN-1 Tracker

高知高専の 2U CubeSat **KOSEN-1**（NORAD 49402）の上空通過を音声でカウントダウンする Web アプリ（iPhone Safari・Android Chrome。案内文は端末に合わせて切り替え）。
ISS 通過カウントダウン（ISS-Alert）をベースにしています。

公開ページ: https://kosen-1.github.io/KOSEN-1_Tracker/

- 観測地点: 高知高専（33.573751°N, 133.649511°E, 20 m）、仰角 3° 以上、3 日間のパスを予測
- 目標は「AOS（受信開始）」（既定）または「最大仰角」を選択
- 5 分前から 5 秒ごとに「あと○秒」、通過後 5 分間「○秒経過」を読み上げ
- 地図に現在位置・地上軌跡・可視範囲を表示
- 右上の「日本語 / EN」で表示と読み上げの言語を切り替え（選択は端末に記憶。初回はブラウザの言語で決定）

## TLE の取得順

1. 端末に保存した TLE（2 時間以内）
2. CelesTrak
3. このリポジトリの `tle.txt`（GitHub Actions が 6 時間ごとに CelesTrak / SatNOGS から更新）
4. 端末に保存した古い TLE
