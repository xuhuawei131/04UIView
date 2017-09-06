# 04UIView


-(void)createView{<br/>
    //UIView 是所有显示在屏幕上 view对象的基础类<br/>
    //所有显示在屏幕上的view 都继承自UIView<br/>
    //UIView 是一个矩形  可以设置背景颜色  有层级关系<br/>
    UIView* view=[[UIView alloc]init];<br/>
    //设置宽高一级位置<br/>
    view.frame=CGRectMake(100, 100, 100, 200);<br/>
    
    [view setBackgroundColor:[UIColor blueColor]];<br/>
    //将新建的视图 添加到 父识图上面<br/>
    [self.view addSubview:view];<br/>
    
    
    //隐藏起来的方法<br/>
    //1、隐藏view  默认值为false 显示出来<br/>
    view.hidden=FALSE;<br/>
    
    view.alpha=0.5;//2、不透明， 如果等于0 那么就是透明的 那么相当于隐藏起来了，如果是0.5那么就是半透明<br/>
    
    [self.view setBackgroundColor:[UIColor greenColor]];<br/>
    //3、是否显示 透明
    view.opaque=NO;
    
    //4、将自己从父view中删除
    [view removeFromSuperview];
}


- (void)viewDidLoad {<br/>
    [super viewDidLoad];<br/>
    [self createView];<br/>
    // Do any additional setup after loading the view, typically from a nib.
}
