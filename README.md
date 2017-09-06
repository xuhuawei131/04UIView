# 04UIView


-(void)createView{
    //UIView 是所有显示在屏幕上 view对象的基础类
    //所有显示在屏幕上的view 都继承自UIView
    //UIView 是一个矩形  可以设置背景颜色  有层级关系
    UIView* view=[[UIView alloc]init];
    //设置宽高一级位置
    view.frame=CGRectMake(100, 100, 100, 200);
    
    [view setBackgroundColor:[UIColor blueColor]];
    //将新建的视图 添加到 父识图上面
    [self.view addSubview:view];
    
    
    //隐藏起来的方法
    //1、隐藏view  默认值为false 显示出来
    view.hidden=FALSE;
    
    view.alpha=0.5;//2、不透明， 如果等于0 那么就是透明的 那么相当于隐藏起来了，如果是0.5那么就是半透明
    
    [self.view setBackgroundColor:[UIColor greenColor]];
    //3、是否显示 透明
    view.opaque=NO;
    
    //4、将自己从父view中删除
    [view removeFromSuperview];
}


- (void)viewDidLoad {
    [super viewDidLoad];
    [self createView];
    // Do any additional setup after loading the view, typically from a nib.
}
