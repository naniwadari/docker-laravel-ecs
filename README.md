# docker-laravel-ecs

laravel を ecs で運用するテスト

## 参考

- https://qiita.com/ken-s/items/3548568eaff4e60c2cb9
- https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4

## 変更点

### ./docker/php/Dockerfile

a

- apk でバージョン指定していた場合エラーが出たためバージョン指定を解除
- `composer global require hirak/prestissimo` 左記パッケージは composer2.0 からは動作しないためエラーになるので削除。

### ./docker-compose

- `${APP_PORT}`にデフォルト値を追加

### docker のビルド

- docker build -t "ファイル名":"タグ" -f "dockerfile のパス" "context のパス"
