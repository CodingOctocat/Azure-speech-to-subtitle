# Azure-speech-to-subtitle
Speech-to-Subtitle (word-level timestamp) code snippet based on MS [Azure Speech](https://github.com/Azure-Samples/cognitive-services-speech-sdk).

> 基于微软 [Azure Speech](https://github.com/Azure-Samples/cognitive-services-speech-sdk) 的语音转字幕（字词级时间戳）的代码片段。

## How my algorithm differs from `RequestWordLevelTimestamps()`?

> ## 我的算法与使用 `RequestWordLevelTimestamps()` 有何不同？

> The `DetailedSpeechRecognitionResult.Words` property of the detailed output message obtained by `RequestWordLevelTimestamps()` is `LexicalForm` and contains profanity.

> `RequestWordLevelTimestamps()` 获取的详细输出信息的 `DetailedSpeechRecognitionResult.Words` 属性内容是 `LexicalForm`，并且包含亵渎性语言。

> Another difference is that the final result of my algorithm is that words are consecutive with no tiny time gaps between them, i.e. `Word.Begin = PreviousWord.End`.
> 
> 另一个差异是，我的算法最终的结果是：单词之间是连续的，没有微小的时间空隙，即 `Word.Begin = PreviousWord.End`。

Code snippets in my gist:

> 代码片段在我的 gist:

[https://gist.github.com/CodingOctocat/3d80252fd59d3895cae7ab370afd442e](https://gist.github.com/CodingOctocat/3d80252fd59d3895cae7ab370afd442e)

**Demo(Not included in gist/repo):**

> **Demo(不包含在 gist/仓库):**

![azure speech to subtitle word level timestamp](https://user-images.githubusercontent.com/7220248/158997209-a5261b36-c0b2-449a-88a1-f1bcf4a1d148.png)
