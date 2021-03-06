# 第三章 根目录文件系统

## 3.1 目的

根文件系统包含的文件必须足以引导（来启动系统）、还原、恢复(和/或)修复系统

- 要通过引导启动系统，根部分必须有足够的软件和数据去安放其他文件系统。这包括实用程序、配置、引导加载程序信息和其他基本用于启动阶段的数据。/usr、/opt 和 /var 的设计使它们可能位于其他分区或文件系统。 
- 为了能够恢复（和/或）修复系统，具有诊断错误和重建损坏的系统功能的系统必须存在于根文件系统上，以便有经验的维护者。
- 为了方便还原系统，从系统备份（软盘、磁带等）恢复所需的实用程序必须位于根文件系统上。

  #### Rationale

  根文件系统的最低要求应尽可能小，但是不能为小而小。虽然许多用户可能不希望分区系统具有额外的复杂性，但出于以下几个原因，应保留保持根目录较小的标准：

  - 它偶尔从非常小的介质中被安装
  - 根文件系统包含许多特定于系统的配置文件。比如说特定于系统的内核、特定主机名等，这意味着根文件系统并不总是可以在网络系统之间共享。在网络化系统的服务器上保持较小的空间可以最大限度地减少私有文件区域带来的空间损失（成本增加）。保持根目录较小允许工作站去使用较小的本地硬盘驱动器（节约成本）。
  - 虽然您可能将根文件系统放在一个大分区上，并且让根目录系统将其完全填满，但也会有人使用较小的分区。当下载大量文件后，如果假设根文件系统在一个大分区下，那么使用较小的分区的人会出问题，反之如果一开始就假设在较小的分区下，那将没有问题（顶多浪费一些空间）。如果您是一名开发人员，那么您的假设带来的问题演变成大量用户的问题。
  - 由于根文件系统上数据损坏引发的磁盘错误比任何其他分区上的错误更严重，而小型根文件系统不太容易因系统崩溃而损坏。

  为了使引导程序可以故障恢复情况下保持正常运行，必须将这些考虑因素与将操作环境弄的尽量小的需求平衡。