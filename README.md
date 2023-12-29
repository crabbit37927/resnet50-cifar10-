# pytorch-resnet50 and cifar-10
<h2>写在前面</h2>
<p>仓库持有者是SZU22级交通专业学生，仅用此仓库记录我的学习生活——to crabbit</p>
<h2>概述</h2>
<p>通过pytorch里面的resnet50模型实现对cifar-10数据集的分类，并将混淆矩阵和部分特征图可视化。</p>
<p>最终测试集的准确率达到95%以上。</p>
<p>辅以另外两个网络googlenet和densenet与resnet50进行对比</p>
<h2>环境配置</h2>
<p>python版本3.9<br>cuda版本11.7<br>pytorch版本2.0.0+cu117<br>torchvision版本0.15.2+cu117<br>torchaudio版本0.13.1+cu117
<h2>代码组成</h2>
<ul>
  <li><h3>main.py</h3></li>
  <p>用于运行主程序</p>
  <li><h3>get_data.py</h3></li>
  <p>用于下载cifar-10数据，并对数据进行预处理</p>
  <li><h3>modle.py</h3></li>
  <p>用于训练与测试模型</p>
  <li><h3>visual.py</h3></li>
  <p>进行所有可视化操作，包括训练过程中acc-loss的变化曲线，测试集的混淆矩阵<br>
    当模型选择为resnet时，会在模型训练后挑选十张图片，输出原图与预测结果，如果预测正确，字体颜色为绿，反之为红。<br>
    此外，还会挑选一张照片，显示模型训练完毕后，在每一层的部分特征图
  </p>
  <p><i>该项目中的混淆矩阵对y轴进行了翻转操作，请注意</i></p>
</ul>
