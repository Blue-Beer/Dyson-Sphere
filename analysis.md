# Analysis of the DYSON-SPHERE

## workflow in the game

1. confirm a list of tasks

2. build a pipeline for the required productions

3. make sure the energy support is available

4. input material to the max capacity of this pipeline

5. consume the production to complete the task

## 设计核心

一个产线系统的运行效率会受到多方面因素的影响，为了让设计思路清晰，我们默认固定的设计前提所有的系统满足一个单元的productionUnitImport是最大值，但是不需要考虑如何达到这个最大值。

## productionUnitImport

一个产线系统的productionUnitImport由多种因素决定。我们需要考虑多个效率：运输效率，分拣效率等等。 这些效率的最小值决定了一个产线系统的输入效率。

但是对于一类特殊的设备——资源采集设备如矿脉和原油采集，这类设备的输入会随时间降低，不受人工设备设计的控制，所以对于这类设施，我们不把它看作产线系统，而是作为运输一种特殊的运输系统。
对于这种运输系统，我们要保证其设备群的产出效率总和大于整数倍的传送设备效率，如传送带的最大运输效率。

