### AbstractQueuedSynchronizer



- AQS 使用一个 Volatile 的 int 类型的成员变量来表示同步状态，通过内置的 FIFO 队列来完成资源获取的排队工作，通过 CAS 完成对 State 值的修改；用于展示当前临界资源的获锁情况。
  - volatile:
    - 保证变量的内存可见性
    - 禁止指令重排序

~~~java
    /**
     * The synchronization state.
     */
    private volatile int state;
~~~

