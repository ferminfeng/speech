## 语音合成SDK

## 安装
```shell
composer require fyflzjz/paypal "v0.0.1"
```



demo

```
$app_id = 'app id';
$app_key = 'app key';
$secret_key = 'secret key';
$log_path = '';
$client = new \fyflzjz\speech\Baidu\AipSpeech($app_id, $app_key, $secret_key, $log_path);
$result = $client->synthesis('你好百度', 'zh',1,['vol' => 5,]);

// 识别正确返回语音二进制 错误则返回json 参照下面错误码
if (!is_array($result)) {
	file_put_contents('audio.mp3', $result);
}
```





参照百度官方文档
http://ai.baidu.com/docs#/TTS-Online-PHP-SDK/top