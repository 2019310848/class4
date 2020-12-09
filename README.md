# class4
java实验
# 实验目的
1. 掌握字符串String及其方法的使用
2. 掌握文件的读取/写入方法
3. 掌握异常处理结构
# 实验过程
1. 先跟上次实验一样先用Scanner来编辑学生的信息
2. 处理后的作业信息，利用字符串处理把输入的长恨歌诗词整理工整，使得诗句间对齐，每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
3. 以防操作时会出现异常，在程序中设计时加入异常处理程序
4. 运行并检查错误
# 实验结果
汉皇重色思倾国，御宇多年求不得。
杨家有女初长成，养在深闺人未识。
天生丽质难自弃，一朝选在君王侧。
回眸一笑百媚生，六宫粉黛无颜色。
春寒赐浴华清池，温泉水滑洗凝脂。
侍儿扶起娇无力，始是新承恩泽时。
云鬓花颜金步摇，芙蓉帐暖度春宵。
春宵苦短日高起，从此君王不早朝。
承欢侍宴无闲暇，春从春游夜专夜。
后宫佳丽三千人，三千宠爱在一身。
金屋妆成娇侍夜，玉楼宴罢醉和春。
姊妹弟兄皆列士，可怜光采生门户。
遂令天下父母心，不重生男重生女。
骊宫高处入青云，仙乐风飘处处闻。
缓歌慢舞凝丝竹，尽日君王看不足。
渔阳鼙鼓动地来，惊破霓裳羽衣曲。
九重城阙烟尘生，千乘万骑西南行。
<未完，待续>，
请输入要查询的字符：
3
******************学生信息*********************
姓名:啦啦啦
年龄:19
编号:2019111111
性别:男
处理完成
3出现的次数为：3次
# 核心方法
用Scanner编入学生信息
```
public class experiment_5 {
    public static void main(String args[]) {
        Scanner input = new Scanner(System.in);
        int w;
        StringBuffer str2 = null;
        Handle las = new Handle();
        StringBuffer str1 = las.Read();
        Homework one = new Homework();
        str2 = one.HW(str1);
        Handle.Write(str2);

        System.out.println("要查询的字符：");
        String z = input.next();
        w = la.getCharMaps(z,str1);

        System.out.println("******************学生信息*********************");
        Student la = new Student();
        la.setName("啦啦啦");
        la.setAge(19);
        la.setNumber(2019111111);
        la.setSex("男");
        System.out.println("姓名:" + la.getName());
        System.out.println("年龄:" + la.getAge());
        System.out.println("编号:" + la.getNumber());
        System.out.println("性别:" + la.getSex());

        System.out.println("处理完成");
        System.out.println(z + "出现的次数为："+ z + "次");
    }
}
```
在文章中插入“，”与“。”
```
class Homework{
    public static StringBuffer HW(StringBuffer str1){
        StringBuffer str2 = new StringBuffer(str1);
        int j=0;int z;
        for(int i = 7;i < str2.length()-45;i= i+7){
            z = i +j;
            if(i%2 == 0){
                str2.insert(z,"。\n");
                j = j+2;
            }
            else{
                str2.insert(z,"，");
                j= j+1;
            }
        }
        System.out.println(str2);
        return str2;
    }

}
```

# 实验感想
通过这次实验，掌握了字符串的用法，学会并应用到了如何为一篇文章快速的增加标点符号，还能够准确地统计出想要查询汉字的出现次数，又一次复习了一遍用Scanner输入信息。因为要把处理好的结果写入到另外的文件夹的过程中遇到了问题，向别的同学请教了一下如何解决，学会了怎么向文件里追加内容。
