# WindowsのNTP時刻同期の設定を変えるregファイル
* WindowsのNTP時刻同期の設定をいいかんじにします

## ファイル説明

### `ntp_mfeed_9h.reg`
* 9時間毎に`ntp.jst.mfeed.ad.jp`と時刻同期します
* 時刻のずれが16秒以内の時はslewモード、それ以上の時はstepモードになります

### `ntp_nict_9h.reg`
* 9時間毎に`ntp.nict.jp`と時刻同期します
* 時刻のずれが16秒以内の時はslewモード、それ以上の時はstepモードになります

### `ntp_nict_for_server.reg`
* `ntp.nict.jp`と時刻同期します
* RFC1305に準拠した間隔での同期（安定性に応じて64秒毎～1024秒毎の間で変化します）
* サーバー向け

### `w32time_autostart.bat`
* W32Timeサービスを自動起動するように設定します
* 管理者権限で実行してください
