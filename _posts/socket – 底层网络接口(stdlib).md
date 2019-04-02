文末附上本文重点：实用Python库大全。

这些框架都需要详细阅读源码，认真理解


**网络**

urllib -网络库(stdlib)。

requests -网络库。

grab – 网络库（基于pycurl）。

pycurl – 网络库（绑定libcurl）。

urllib3 – Python HTTP库，安全连接池、支持文件post、可用性高。

httplib2 – 网络库。

RoboBrowser – 一个简单的、极具Python风格的Python库，无需独立的浏览器即可浏览网页。

MechanicalSoup -一个与网站自动交互Python库。

mechanize -有状态、可编程的Web浏览库。

socket – 底层网络接口(stdlib)。


**文本处理**

用于解析和操作简单文本的库。

difflib – （Python标准库）帮助进行差异化比较。

Levenshtein – 快速计算Levenshtein距离和字符串相似度。

fuzzywuzzy – 模糊字符串匹配。

esmre – 正则表达式加速器。

ftfy – 自动整理Unicode文本，减少碎片化。


**多重处理**

threading – Python标准库的线程运行。对于I/O密集型任务很有效。对于CPU绑定的任务没用，因为python GIL。

multiprocessing – 标准的Python库运行多进程。

celery – 基于分布式消息传递的异步任务队列/作业队列。

concurrent-futures – concurrent-futures 模块为调用异步执行提供了一个高层次的接口。

**异步**

异步网络编程库

asyncio – （在Python 3.4 +版本以上的 Python标准库）异步I/O，时间循环，协同程序和任务。

Twisted – 基于事件驱动的网络引擎框架。

Tornado – 一个网络框架和异步网络库。

pulsar – Python事件驱动的并发框架。

diesel – Python的基于绿色事件的I/O框架。

gevent – 一个使用greenlet 的基于协程的Python网络库。

eventlet – 有WSGI支持的异步框架。

Tomorrow – 异步代码的奇妙的修饰语法。

**队列**

celery – 基于分布式消息传递的异步任务队列/作业队列。

huey – 小型多线程任务队列。

mrq – Mr. Queue – 使用redis & Gevent 的Python分布式工作任务队列。

RQ – 基于Redis的轻量级任务队列管理器。

simpleq – 一个简单的，可无限扩展，基于Amazon SQS的队列。

python-gearman – Gearman的Python API。

**云计算**

picloud – 云端执行Python代码。

dominoup.com – 云端执行R，Python和matlab代码

网页内容提取

提取网页内容的库。

HTML页面的文本和元数据

newspaper – 用Python进行新闻提取、文章提取和内容策展。

html2text – 将HTML转为Markdown格式文本。

python-goose – HTML内容/文章提取器。

lassie – 人性化的网页内容检索工具



