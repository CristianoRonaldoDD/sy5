综合性实验 学生选课系统
==========
实验目的
--------
1、分析学生选课系统<br>
2、使用GUI窗体及其组件设计窗体界面<br>
3、完成学生选课过程业务逻辑编程
4、基于文件保存并读取数据<br>
5、异常处理<br>

实验内容
--------
一、系统角色分析及类设计<br>
属性实例：人员（编号、姓名、性别....）<br>
         教师（编号、姓名、性别、所授课程....）<br>
         学生（编号、姓名、性别、所选课程....）<br>
         课程（编号、课程名称、上课地点、时间、授课教师....）<br>
         
实验步骤
-------
1、登录窗口 输入用户名及密码，输出错误信息，用if条件进行判断<br>
2、输入学生信息、老师信息、课程信息<br>
3、学生选课、退课、课表查询<br>

核心代码
--------
```
setTitle("Welcome");
  setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
  setBounds(100, 100, 450, 300);

```
登陆界面
```
Label label = new Label("课程编号: ");
  label.setFont(new Font("PLAIN", Font.BOLD | Font.ITALIC, 12));
  GridBagConstraints gbc_label = new GridBagConstraints();
  gbc_label.insets = new Insets(0, 0, 5, 5);
  gbc_label.gridx = 0;
  gbc_label.gridy = 1;
  
  ```
创建课程信息:课程编号、课程名字、课程地点、课程老师等<br>
```
setTitle("Chose Classes");
  setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
  setBounds(100, 100, 800, 400);
  contentPane = new JPanel();
  contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
  setContentPane(contentPane);
  GridBagLayout gbl_contentPane = new GridBagLayout();
  gbl_contentPane.columnWidths = new int[]{185, 136, 0};
  gbl_contentPane.rowHeights = new int[]{51, 86, 0};
  gbl_contentPane.columnWeights = new double[]{1.0, 0.0, Double.MIN_VALUE};
  gbl_contentPane.rowWeights = new double[]{0.0, 1.0, Double.MIN_VALUE};

```
选课界面<br>
```
setTitle("Exit Classes");
  setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
  setBounds(100, 100, 800, 400);
  contentPane = new JPanel();
  contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
  setContentPane(contentPane);
  GridBagLayout gbl_contentPane = new GridBagLayout();
  gbl_contentPane.columnWidths = new int[]{809, 100, 0};
  gbl_contentPane.rowHeights = new int[]{53, 40, 0};
  gbl_contentPane.columnWeights = new double[]{1.0, 0.0, Double.MIN_VALUE};
  gbl_contentPane.rowWeights = new double[]{0.0, 1.0, Double.MIN_VALUE};
```
退课界面<br>
```
public Index() {
  setTitle("主页");
  setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
  setBounds
  (150, 150, 500, 350);
  contentPane = new JPanel();
  contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
  setContentPane(contentPane);
  contentPane.setLayout(null);
  JButton btnNewButton = new JButton("退课");
  btnNewButton.setBounds(175, 0, 97, 23);
  contentPane.add(btnNewButton);
  btnNewButton.addActionListener(new ActionListener(){
   public void actionPerformed(ActionEvent e) {
    Exit exit = new Exit();
    exit.setVisible(true);
   }
  });
  JButton btnNewButton_1 = new JButton("选课");
  btnNewButton_1.setBounds(175, 107, 97, 23);
  contentPane.add(btnNewButton_1);
  btnNewButton_1.addActionListener(new ActionListener(){
   public void actionPerformed(ActionEvent e) {
    Chose chose = new Chose();
    chose.setVisible(true); 
   }
  });
  JButton btnNewButton_3 = new JButton("打印");
  btnNewButton_3.setBounds(175, 200, 97, 23);
  contentPane.add(btnNewButton_3);
  btnNewButton_3.addActionListener(new ActionListener(){
   public void actionPerformed(ActionEvent e) {
    Print print = new Print();
    print.setVisible(true);
```

实验结果
-------
![](https://github.com/CristianoRonaldoDD/sy5/blob/master/%E6%8D%951%E8%8E%B7.PNG)</div>
![]()</div>

感想
----
对GUI的编程还不熟悉，需要请教老师同学·查阅资料才能完成，还需努力。
