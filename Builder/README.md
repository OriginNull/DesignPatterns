## 建造者模式
* 指将一个复杂对象的构造与它的表示分离，使同样的构建过程可以创建不同的表示。它将一个复杂的对象分解为多个简单的对象，然后一步一步构建而成。将变与不变相分离，即产品的组成部分是不变的，但每一部分是可以灵活选择的。建造者模式注重零部件的组装过程
* 建造者（Builder）模式的主要角色如下。
    * 产品角色（Product）：它是包含多个组成部件的复杂对象，由具体建造者来创建其各个部件。
    * 抽象建造者（Builder）：它是一个包含创建产品各个子部件的抽象方法的接口，通常还包含一个返回复杂产品的方法 getResult()。
    * 具体建造者(Concrete Builder）：实现 Builder 接口，完成复杂产品的各个部件的具体创建方法。
    * 指挥者（Director）：它调用建造者对象中的部件构造与装配方法完成复杂对象的创建，在指挥者中不涉及具体产品的信息。
* 适用于 创建的对象较复杂，由多个部件构成，各部件面临着复杂的变化，但构件间的建造顺序是稳定的。比如OpenCV的绘制，大致的绘制操作流程是一样的，但是具体每一步的绘制细节可能不一样，比如绘制三角形和绘制正方形。