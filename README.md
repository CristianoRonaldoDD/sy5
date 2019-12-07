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
setTitle("欢迎光临");
  setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
  setBounds(100, 100, 450, 300);

```
登陆界面
```
Label label = new Label("课程号: ");
  label.setFont(new Font("PLAIN", Font.BOLD | Font.ITALIC, 12));
  GridBagConstraints gbc_label = new GridBagConstraints();
  gbc_label.insets = new Insets(0, 0, 5, 5);
  gbc_label.gridx = 0;
  gbc_label.gridy = 1;
  
  ```
设置课程:课程编号、课程名字、课程地点、课程时间等<br>
```
public Create() {
		setTitle("Create Classes");
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 450, 300);
		contentPane = new JPanel();
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		setContentPane(contentPane);
		GridBagLayout gbl_contentPane = new GridBagLayout();
		gbl_contentPane.columnWidths = new int[]{93, 142, 164, 0};
		gbl_contentPane.rowHeights = new int[]{0, 0, 0, 0, 0, 0, 0, 0, 0};
		gbl_contentPane.columnWeights = new double[]{1.0, 0.0, 0.0, Double.MIN_VALUE};
		gbl_contentPane.rowWeights = new double[]{1.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 1.0, Double.MIN_VALUE};
		contentPane.setLayout(gbl_contentPane);
		
		Label label = new Label("Class Number: ");
		label.setFont(new Font("Calibri", Font.BOLD | Font.ITALIC, 12));
		GridBagConstraints gbc_label = new GridBagConstraints();
		gbc_label.insets = new Insets(0, 0, 5, 5);
		gbc_label.gridx = 0;
		gbc_label.gridy = 1;
		contentPane.add(label, gbc_label);
		// Create Label
		TextField textField = new TextField();
		GridBagConstraints gbc_textField = new GridBagConstraints();
		gbc_textField.fill = GridBagConstraints.BOTH;
		gbc_textField.insets = new Insets(0, 0, 5, 5);
		gbc_textField.gridx = 1;
		gbc_textField.gridy = 1;
		contentPane.add(textField, gbc_textField);
		// Create textField
		Label label_1 = new Label("Class Name: ");
		label_1.setFont(new Font("Calibri", Font.BOLD | Font.ITALIC, 12));
		GridBagConstraints gbc_label_1 = new GridBagConstraints();
		gbc_label_1.insets = new Insets(0, 0, 5, 5);
		gbc_label_1.gridx = 0;
		gbc_label_1.gridy = 2;
		contentPane.add(label_1, gbc_label_1);
		
		TextField textField_1 = new TextField();
		GridBagConstraints gbc_textField_1 = new GridBagConstraints();
		gbc_textField_1.fill = GridBagConstraints.BOTH;
		gbc_textField_1.insets = new Insets(0, 0, 5, 5);
		gbc_textField_1.gridx = 1;
		gbc_textField_1.gridy = 2;
		contentPane.add(textField_1, gbc_textField_1);
		
		Label label_2 = new Label("Class Place: ");
		label_2.setFont(new Font("Cambria", Font.BOLD | Font.ITALIC, 12));
		GridBagConstraints gbc_label_2 = new GridBagConstraints();
		gbc_label_2.insets = new Insets(0, 0, 5, 5);
		gbc_label_2.gridx = 0;
		gbc_label_2.gridy = 3;
		contentPane.add(label_2, gbc_label_2);
		
		TextField textField_2 = new TextField();
		GridBagConstraints gbc_textField_2 = new GridBagConstraints();
		gbc_textField_2.fill = GridBagConstraints.BOTH;
		gbc_textField_2.insets = new Insets(0, 0, 5, 5);
		gbc_textField_2.gridx = 1;
		gbc_textField_2.gridy = 3;
		contentPane.add(textField_2, gbc_textField_2);
		
		Label label_3 = new Label("Class Time: ");
		label_3.setFont(new Font("Cambria", Font.BOLD | Font.ITALIC, 12));
		GridBagConstraints gbc_label_3 = new GridBagConstraints();
		gbc_label_3.insets = new Insets(0, 0, 5, 5);
		gbc_label_3.gridx = 0;
		gbc_label_3.gridy = 4;
		contentPane.add(label_3, gbc_label_3);
		
		TextField textField_3 = new TextField();
		GridBagConstraints gbc_textField_3 = new GridBagConstraints();
		gbc_textField_3.fill = GridBagConstraints.BOTH;
		gbc_textField_3.insets = new Insets(0, 0, 5, 5);
		gbc_textField_3.gridx = 1;
		gbc_textField_3.gridy = 4;
		contentPane.add(textField_3, gbc_textField_3);
		
		Label label_4 = new Label("Class Credit: ");
		label_4.setFont(new Font("Cambria", Font.BOLD | Font.ITALIC, 12));
		GridBagConstraints gbc_label_4 = new GridBagConstraints();
		gbc_label_4.insets = new Insets(0, 0, 5, 5);
		gbc_label_4.gridx = 0;
		gbc_label_4.gridy = 5;
		contentPane.add(label_4, gbc_label_4);
		
		TextField textField_4 = new TextField();
		GridBagConstraints gbc_textField_4 = new GridBagConstraints();
		gbc_textField_4.fill = GridBagConstraints.BOTH;
		gbc_textField_4.insets = new Insets(0, 0, 5, 5);
		gbc_textField_4.gridx = 1;
		gbc_textField_4.gridy = 5;
		contentPane.add(textField_4, gbc_textField_4);
		
		Label label_5 = new Label("Class Teacher: ");
		label_5.setFont(new Font("Calibri", Font.BOLD | Font.ITALIC, 12));
		GridBagConstraints gbc_label_5 = new GridBagConstraints();
		gbc_label_5.insets = new Insets(0, 0, 5, 5);
		gbc_label_5.gridx = 0;
		gbc_label_5.gridy = 6;
		contentPane.add(label_5, gbc_label_5);
		
		TextField textField_5 = new TextField();
		GridBagConstraints gbc_textField_5 = new GridBagConstraints();
		gbc_textField_5.fill = GridBagConstraints.BOTH;
		gbc_textField_5.insets = new Insets(0, 0, 5, 5);
		gbc_textField_5.gridx = 1;
		gbc_textField_5.gridy = 6;
		contentPane.add(textField_5, gbc_textField_5);

		Button button = new Button("Create Lessons"); //set Button name
		button.setFont(new Font("Calibri", Font.BOLD | Font.ITALIC, 18)); // set font
		GridBagConstraints gbc_button = new GridBagConstraints();
		gbc_button.fill = GridBagConstraints.BOTH; //layout
		gbc_button.gridx = 2;
		gbc_button.gridy = 7; //position
		contentPane.add(button, gbc_button);
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
  (160, 160, 490, 410);
  contentPane = new JPanel();
  contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
  setContentPane(contentPane);
  contentPane.setLayout(null);
  JButton btnNewButton = new JButton("退课");
  btnNewButton.setBounds(170, 0, 97, 24);
  contentPane.add(btnNewButton);
  btnNewButton.addActionListener(new ActionListener(){
   public void actionPerformed(ActionEvent e) {
    Exit exit = new Exit();
    exit.setVisible(true);
   }
  });
  JButton btnNewButton_1 = new JButton("选课");
  btnNewButton_1.setBounds(170, 107, 97, 24);
  contentPane.add(btnNewButton_1);
  btnNewButton_1.addActionListener(new ActionListener(){
   public void actionPerformed(ActionEvent e) {
    Chose chose = new Chose();
    chose.setVisible(true); 
   }
  });
  JButton btnNewButton_3 = new JButton("打印");
  btnNewButton_3.setBounds(170, 200, 97, 24);
  contentPane.add(btnNewButton_3);
  btnNewButton_3.addActionListener(new ActionListener(){
   public void actionPerformed(ActionEvent e) {
    Print print = new Print();
    print.setVisible(true);
```

实验结果
-------
![](https://github.com/CristianoRonaldoDD/sy5/blob/master/%E6%8D%951%E8%8E%B7.PNG)</div>
![](https://github.com/CristianoRonaldoDD/sy5/blob/master/%E6%8D%95%E8%8E%B72.PNG)</div>

感想
----
对GUI的编程还不熟悉，需要请教老师同学·查阅资料才能完成，还需努力。
