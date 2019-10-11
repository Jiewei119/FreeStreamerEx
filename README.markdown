FreeStreamerEx是从FreeStreamer这个开源的音频播放类库修改扩展而来，主要做了以下修改扩展：
1.提供直接播放NSData类型音频数据的支持；
2.提供播放需要解密mp3音频数据的支持；

如何使用新增的修改扩展功能播放NSData类型音频数据：
1.通过调用FSAudioController类的initWithData:初始化方法进行初始化，然后直接调用该类的play方法即可；
2.直接调用该类的playFromData方法;
3.直接调用该类的playFromPlaylist方法,前提是给传递的FSPlaylistItem之中的data属性赋值即可;

如何使用新增的修改扩展功能播放需要解密mp3音频数据：
只需要创建指定的block，将其赋值给FSAudioController类的audioDataDecrypt属性，在audioDataDecrypt这个block的内部做解密处理即可，注意：解密处理的是本地mp3音频文件。


关于FreeStreamer这个开源的音频播放类库更多的说明，请查看下面原项目的说明：

FreeStreamer
====================

A streaming audio player for iOS and OS X.

Features
====================

- **CPU-friendly** design (uses 1% of CPU on average when streaming)
- **Multiple protocols supported**: ShoutCast, standard HTTP, local files
- **Prepared for tough network conditions**: adjustable buffer sizes, stream pre-buffering and restart on failures
- **Metadata support**: ShoutCast metadata, IDv2 tags
- **Local disk caching**: user only needs to stream a file once and after that it can be played from a local cache
- **Preloading**: playback can start immediately without needing to wait for buffering
- **Record**: support recording the stream contents to a file
- **Access the PCM audio samples**: as an example, a visualizer is included

Documentation
====================

See the [FAQ](https://github.com/muhku/FreeStreamer/wiki/FreeStreamer-FAQ) (Frequently Asked Questions) in the wiki. We also have an [API documentation](http://muhku.github.io/api/) available. The [usage instructions](https://github.com/muhku/FreeStreamer/wiki/Using-the-player-in-your-own-project) are also covered in the wiki.

Is somebody using this in real life?
====================

The short answer is yes! Check out our [website](http://muhku.github.io/) for the reference applications.

Reporting bugs and contributing
====================

For code contributions and other questions, it is preferrable to create a Github pull request. I don't have time for private email support, so usually the best way to get help is to interact with Github issues.

License
====================

See [LICENSE.txt](https://github.com/muhku/FreeStreamer/blob/master/LICENSE.txt) for the license.

Donations
====================

It is possible to use [PayPal](http://muhku.github.io/donate.html) for donations.
