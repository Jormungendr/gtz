# 更新日志

## v0.1.1

### Bugs修复
修复了解压过程可能的死锁问题。导致问题的根源在于，ID行中的部分数据域过长，会导致一段过度优化的字符串处理代码死锁。
感谢华大基因 陈毓新 的反馈。

## v0.1

### 新特性

* **高压缩比：**采用Context Model压缩技术，配合多种优化的预测模型，平衡系统并发度与内存资源消耗后，能达到极高的压缩率。对FASTQ文件，压缩率最高可达5.58%。

* **高性能：** GTX compressor充分发挥了CPU的并发性以及新型Haswell CPU体系结构与AVX2、BMI2等指令集的计算能力，使得在普通服务器上的压缩速度，最高能够以接近114MB/s的输入流量输入数据并压缩完毕。

* **高速直压上云：** GTX compressor支持直压上云和从云端直接解压下载功能。普通的20核服务器，通过百兆Intenet线路，可以在短短30分钟内稳定地将200GB Fastq文件的直压上云。 




