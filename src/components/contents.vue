<template>
  <div class="contentsContainer">
    <div class="circleContainer">
      <circ class="circleText"> SI-Bench </circ>
    </div>
    <div class="connect">
      <div class="line"></div>
      <div class="horizontolLine"></div>
      <div class="lineGroup">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
    </div>
    <div class="taskContainer">
      <div class="taskItemContainer">
        <div class="task">物体理解</div>
      </div>
      <div class="taskItemContainer"><div class="task">场景理解</div></div>
      <div class="taskItemContainer"><div class="task">空间关系理解</div></div>
      <div class="taskItemContainer"><div class="task">时空关系理解</div></div>
      <div class="taskItemContainer"><div class="task">空间推理</div></div>
      <div class="taskItemContainer"><div class="task">时空推理</div></div>
    </div>
    <div class="connect">
      <div class="lineGroup">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </div>
    </div>
    <div class="subTaskContainer">
      <div class="subTaskGroup">
        <div class="subTask">物体大小估计</div>
        <div class="subTask">物体属性识别</div>
        <div class="subTask">物体可供性识别</div>
      </div>
      <div class="subTaskGroup">
        <div class="subTask">视觉定位</div>
        <div class="subTask">面积估计</div>
        <div class="subTask">绝对距离</div>
        <div class="subTask">场景类别识别</div>
      </div>
      <div class="subTaskGroup">
        <div class="subTask">物体计数</div>
        <div class="subTask">相对方向</div>
        <div class="subTask">相对距离</div>
        <div class="subTask">空间状态记忆</div>
      </div>
      <div class="subTaskGroup">
        <div class="subTask">出现顺序</div>
        <div class="subTask">动作理解</div>
        <div class="subTask">状态变化理解</div>
      </div>
      <div class="subTaskGroup">
        <div class="subTask">路径规划</div>
        <div class="subTask">空间因果预测</div>
      </div>
      <div class="subTaskGroup">
        <div class="subTask">时空因果预测</div>
        <div class="subTask">动态物理预测</div>
      </div>
    </div>
  </div>
  <div class="qandaContainer">
    <div class="qandaItemContainer">
      <div class="qandaItemTitle">物体理解</div>
      <div class="datasetUsed">
        所包含数据组：arkitscenes、scannet、scannet++、3rscan、waymo、nuscenes
      </div>
      <div class="videoDisplayContainer">
        <video
          muted
          playsinline
          loop
          controls
          disable-picture-in-picture="true"
        >
          <source src="" type="video/mp4" />
        </video>
      </div>
      <div class="qanda">
        <div class="q">
          <span class="stress">Q:</span> What is the length of the longest
          dimension (length, width, or height) of the stove, measured in
          centimeters?
        </div>
        <div class="a"><span class="stress">A:</span> 62</div>
      </div>
      <div class="qanda">
        <div class="q">
					.text
          <span class="stress">Q:</span> Given a video of 199 frames, at frame
          26, what is the length of the longest dimension (length, width, or
          height) of a blue sedan in region (0.38,0.54,0.70,0.72)[Note: Bounding
          box region, coordinates are normalized (0~1), format (x1,y1,x2,y2)
          with (0,0)=top-left], measured in centimeters? (Note: The frame rate
          of the video is 10fps)
        </div>
        <div class="a"><span class="stress">A:</span> 467</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import circ from "../utils/circle.vue";
</script>

<style scoped>
.contentsContainer {
  display: flex;
  /* justify-content: center; */
  align-items: center;
  /* flex-direction: column; */
  padding: 5vmax;

  width: 100%;
  height: 80dvh;
  /* height: 100vh; */
  box-sizing: border-box;
}
.circleContainer {
  display: flex;
  width: 200px;
  height: 200px;
  box-sizing: border-box;
  margin-left: 10vw;
}
.circleText {
  font-size: 24px;
  font-family: "PS-bold";
  color: #fff;
}

.connect {
  display: flex;
  position: relative;
  height: 100%;
  width: 10vw;
  box-sizing: border-box;
}
.line {
  align-self: center;
  width: 35%;
  height: 2px;
  background-color: #209cee;
}
.horizontolLine {
  display: flex;
  height: 83.5%;
  width: 2.5px;
  justify-self: center;
  align-self: center;
  box-sizing: border-box;
  background-color: #209cee;
}

.lineGroup {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  padding: 25% 0;
  justify-content: space-between;
  box-sizing: border-box;
}
.lineGroup .line {
  width: 100%;
}

.taskContainer,
.subTaskContainer {
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: space-between;
  box-sizing: border-box;
}

.taskItemContainer {
  display: flex;
  height: 100%;
  align-items: center;
}

.task,
.subTask {
  display: flex;
  height: 1.75vmax;

  justify-content: center;
  align-items: center;
  font-family: "Alibaba-puhui-bold";
  border-radius: 20px;
  border: #209cee solid 2px;
  padding: 0.5vmax 1vmax;
  margin: 0.5vmax;
  font-size: 0.8vmax;
  cursor: pointer;
}
.task {
  color: #ffffff;
  width: 5vmax;
  background-color: #209cee;
}
.task:hover {
  background-color: #63b2e7;
  border: #63b2e7 solid 2px;
}
.subTask {
  color: #209cee;
  background-color: transparent;
}
.subTask:hover {
  background-color: #def2ff;
}
.subTaskGroup {
  display: flex;
  height: 100%;
  align-items: center;
  /* display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr; */
}
.qandaContainer {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 0 15%;
  box-sizing: border-box;
  min-height: 100dvh;
  padding-bottom: 10vmax;
}
.qandaItemContainer {
  display: flex;
  flex-direction: column;
  width: 100%;
  box-sizing: border-box;
  align-items: center;
}
.qandaItemTitle {
  color: #209cee;
  font-family: "Alibaba-puhui-bold";
  font-size: 54px;
}
.datasetUsed {
  color: #63b2e7;
  font-family: "Alibaba-puhui-bold";
  font-size: 20px;
  margin-top: 20px;
}
.videoDisplayContainer {
  display: flex;
  width: 80%;
  margin-top: 20px;
}
video {
  width: 100%;
  aspect-ratio: 16/9;
}
.qanda {
  width: 60%;

  font-family: "Alibaba-puhui-regular";
  font-size: 20px;
  margin-top: 20px;
  line-height: 1.5;
}
.qanda > * {
  margin-top: 18px;
}
.stress {
  font-family: "Alibaba-puhui-bold";
  color: #209cee;
  font-size: 36px;
  margin-right: 8px;
}
</style>
