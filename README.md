这是一个非常简单的, 可以自定义的 andlua UI, 即使是小白也能做出自己喜欢的UI, 控件的ID和文本自己可以加上去, 如果有不懂的可以加我QQ 3539186671


UI示例

悬浮窗配置
```lua
xfc = { -- UI主框架
  LinearLayout;
  id="窗体";
  layout_height="fill";
  layout_width="fill";
  {
    LinearLayout;
    id="WIN1";
    layout_height="250dp";
    backgroundColor="0xFF252525";
    layout_width="350dp";
    {
      LinearLayout;
      id="WIN2";
      layout_height="match_parent";
      orientation="vertical";
      backgroundColor="0xFF2A2A29";
      layout_width="90dp";
      {
        LinearLayout;
        layout_height="70dp";
        orientation="vertical";
        gravity="center";
        paddingTop="10dp";
        layout_width="match_parent";
        {
          CircleImageView; 
          src="res/AzureLoGo.png"; --这是logo, 您可以改成自己的图片
          layout_width="35dp";
          layout_height="35dp";
          id="LoGo";
        };
        {
          TextView;
          gravity="center";
          layout_width="match_parent";
          layout_height="match_parent";
          text="走马观花 v1.0"; -- 标题
          textColor="0xFFFFFFFF";
        };
      };
      {
        ScrollView;
        layout_height="match_parent";
        layout_width="match_parent";
        {
          LinearLayout;
          layout_height="match_parent";
          orientation="vertical";
          gravity="center";
          layout_width="match_parent";
          {
            Button;
            textSize="15sp";
            layout_width="80%w";
            backgroundColor="0x00000000";
            layout_height="40dp";
            text="*    功能1";
            id="功能1";
            textColor="0xFFFFFFFF";
          };
          {
            Button;
            textSize="15sp";
            layout_width="80%w";
            backgroundColor="0x00000000";
            layout_height="40dp";
            text="*    功能2";
            textColor="0xFFFFFFFF";
            id="功能2";
          };
          {
            Button;
            layout_width="80%w";
            textSize="15sp";
            layout_height="40dp";
            backgroundColor="0x00000000";
            text="*    功能3";
            id="功能3";
            textColor="0xFFFFFFFF";
          };
          {
            Button;
            layout_width="80%w";
            textSize="15sp";
            layout_height="40dp";
            backgroundColor="0x00000000";
            text="*    功能4";
            id="功能4";
            textColor="0xFFFFFFFF";
          };
          {
            Button;
            layout_width="80%w";
            textSize="15sp";
            layout_height="40dp";
            backgroundColor="0x00000000";
            text="*    功能5";
            textColor="0xFFFFFFFF";
          };
        };
      };
    };
    {
      LinearLayout;
      layout_height="match_parent";
      backgroundColor="0xFF414141";
      layout_width="match_parent";
      {
        PageView;
        id="pg";
        layout_width="match_parent";
        layout_height="match_parent";
        pages={ -- 一共有多少个界面(滑动窗体框架)
          jm1;
          jm2;
          jm3;
          jm4;
        }; -- endl pages
      };
    };
  };
}
```


悬浮球配置
```lua
xfq = { -- 悬浮球配置
LinearLayout;
  layout_width="fill";
  layout_height="fill";
  {
    CircleImageView;
    src="res/icon.png";
    layout_width="40dp";
    id="图标";
    layout_height="40dp";
  };
}
```

这是一个滑动窗体, 配合悬浮窗使用, 实现多窗口
```lua
    {
      LinearLayout;
      layout_width="fill";
      layout_height="fill";
      {
        LinearLayout;
        layout_width="match_parent";
        layout_height="match_parent";
        {
          ScrollView;
          layout_width="match_parent";
          layout_height="match_parent";
          {
            LinearLayout;
            gravity="top|center";
            orientation="vertical";
            backgroundColor="#353A3D";
            layout_height="match_parent";
            layout_width="match_parent";
           };
         };
       };
    }; -- end 滑动窗体框架
```
Page
```lua
    {
      LinearLayout;
      layout_marginTop="5dp";
      orientation="vertical";
      backgroundColor="#303135";
      layout_height="wrap_content";
      layout_width="68%w";
      {
        TextView;
        layout_width="match_parent";
        textColor="0xFFFFFFFF";
        gravity="left";
        text="	页面名称";
      };
      {
        LinearLayout;
        gravity="top|center";
        layout_width="match_parent";
        layout_height="match_parent";
        orientation="vertical";
      };
    }; -- end 页面
```
按钮控件
```lua
    {
      Button;
      gravity="center";
      textColor="0xFFFFFFFF";
      text="功能一";
      layout_width="68%w";
      backgroundColor="#242529";
      layout_marginTop="5dp";
    }; -- end 按钮
```

开关控件
```lua
    {
      LinearLayout;
      layout_marginTop="5dp";
      orientation="horizontal";
      backgroundColor="#242529";
      layout_height="45dp";
      layout_width="68%w";
      {
        Switch;
        gravity="left|center";
        textColor="0xFFFFFFFF";
        text="开关名称";
        layout_width="match_parent";
        paddingLeft="5dp";
        layout_height="match_parent";
      };
    }; -- end 开关
```

文本盒子
```lua
  {
    LinearLayout;
    layout_width="68%w";
    orientation="horizontal";
    layout_height="45dp";
    layout_marginTop="5dp";
    backgroundColor="#242529";
    {
      TextView;
      textColor="0xFFFFFFFF";
      layout_marginLeft="5dp";
      layout_height="match_parent";
      text="文本盒子"; -- 输入框名字
      gravity="center";
     };
     {
       LinearLayout;
       layout_width="match_parent";
       gravity="center";
       layout_height="match_parent";
     {
        EditText;  --输入框
        layout_width="match_parent";
        hint="请输入数字";
        gravity="center";
        textColor="0xFFFFFFFF";
        hintTextColor="0xFFD6D9D8";
     };
    };
  }; -- end 文本盒子
```

滑块
```lua
    {
      LinearLayout;
      layout_marginTop="5dp";
      orientation="vertical";
      backgroundColor="#242529";
      layout_height="55dp";
      layout_width="68%w";
      {
        LinearLayout;
        orientation="horizontal";
        layout_height="25dp";
        layout_width="match_parent";
        {
          TextView;
          gravity="center";
          textColor="0xFFFFFFFF";
          layout_height="match_parent";
          text="    滑块名称";
        };
        {
          LinearLayout;
          gravity="right|center";
          layout_height="match_parent";
          layout_width="match_parent";
          {
            TextView; -- 滑块显示的数字
            gravity="center";
            textColor="0xFFFFFFFF";
            text="100";
            layout_marginRight="5dp";
            layout_height="match_parent";
          };
        };
      };
      {
        LinearLayout;
        layout_width="match_parent";
        layout_height="match_parent";
        {
          SeekBar; -- 滑块本体
          layout_width="match_parent";
          layout_height="match_parent";
          max="300";
        };
      };
    }; -- end 滑块
```

悬浮窗移动配置
```lua
import "android.content.Context"
import "android.provider.Settings"
import "android.animation.ObjectAnimator"
import "android.animation.ArgbEvaluator"
import "android.animation.ValueAnimator"
import "android.graphics.Color"
import "android.content.Intent"
import "android.net.Uri"
import "android.graphics.PixelFormat"
import "AndLua"
import "android.graphics.PorterDuff"
import "android.graphics.PorterDuffColorFilter"

wmManager=activity.getSystemService(Context.WINDOW_SERVICE) --获取窗口管理器
HasFocus=false --是否有焦点
wmParams =WindowManager.LayoutParams() --对象
if tonumber(Build.VERSION.SDK) >= 26 then
  wmParams.type =WindowManager.LayoutParams.TYPE_APPLICATION_OVERLAY--安卓8以上悬浮窗打开方式
 else
  wmParams.type =WindowManager.LayoutParams.TYPE_SYSTEM_ALERT--安卓8以下的悬浮窗打开方式
end
wmParams.format =PixelFormat.RGBA_8888 --设置背景
wmParams.flags=WindowManager.LayoutParams().FLAG_NOT_FOCUSABLE--焦点设置
wmParams.gravity = Gravity.LEFT| Gravity.TOP --重力设置
wmParams.x = activity.getWidth()/6
wmParams.y = activity.getHeight()/5
wmParams.width =WindowManager.LayoutParams.WRAP_CONTENT
wmParams.height =WindowManager.LayoutParams.WRAP_CONTENT
if Build.VERSION.SDK_INT >= Build.VERSION_CODES.M&&!Settings.canDrawOverlays(this) then
  print("没有悬浮窗权限悬，请打开权限")
  intent=Intent(Settings.ACTION_MANAGE_OVERLAY_PERMISSION)
  intent.setData(Uri.parse("package:" .. activity.getPackageName()));
  activity.startActivityForResult(intent, 100)
  os.exit()
 else

  悬浮球=loadlayout(xfq)--悬浮球
  悬浮窗=loadlayout(xfcs)--悬浮窗
end

控件圆角(WIN1, 0xFF252525, 10)
控件圆角(WIN2, 0xFF252525, 10)

开启.onTouch=function()--开启悬浮窗代码
  if 悬浮球是否打开 == nil then
    wmManager.addView(悬浮球,wmParams)
    悬浮球是否打开=true
   else
    print("你已启动悬浮窗！")
    -- MD提示("你以启动悬浮窗",0xFF2196F3,0xFFFFFFFF,4,10)
  end
end


function 图标.onClick()--放大悬浮窗代码
  wmManager.addView(悬浮窗,wmParams )
  wmManager.removeView(悬浮球)
end

function LoGo.onClick() -- 点击logo隐藏悬浮窗
  wmManager.removeView(悬浮窗)
  wmManager.addView(悬浮球,wmParams)
  print("已隐藏");
end

function LoGo.onLongClick() -- 长按logo关闭悬浮窗
  wmManager.removeView(悬浮窗)
  悬浮球是否打开=nil
  print("已退出");
end


function 图标.OnTouchListener(v,event)--这个图标移动代码
  if event.getAction()==MotionEvent.ACTION_DOWN then
    firstX=event.getRawX()
    firstY=event.getRawY()
    wmX=wmParams.x
    wmY=wmParams.y
   elseif event.getAction()==MotionEvent.ACTION_MOVE then
    wmParams.x=wmX+(event.getRawX()-firstX)
    wmParams.y=wmY+(event.getRawY()-firstY)
    wmManager.updateViewLayout(悬浮球,wmParams)
   elseif event.getAction()==MotionEvent.ACTION_UP then
  end
  return false
end

function 窗体.OnTouchListener(v,event)--这个图标移动代码
  if event.getAction()==MotionEvent.ACTION_DOWN then
    firstX=event.getRawX()
    firstY=event.getRawY()
    wmX=wmParams.x
    wmY=wmParams.y
   elseif event.getAction()==MotionEvent.ACTION_MOVE then
    wmParams.x=wmX+(event.getRawX()-firstX)
    wmParams.y=wmY+(event.getRawY()-firstY)
    wmManager.updateViewLayout(悬浮窗,wmParams)
   elseif event.getAction()==MotionEvent.ACTION_UP then
  end
  return false
end

-- 下面这个是 page滑动点击按钮显示界面的事件

pg.addOnPageChangeListener{
  onPageScrolled=function(a,b,c)
    -- 在滑动的时候不断调用 a,b,c
  end,
  onPageSelected = function(page)
    if IsDebug then
      print(page)
    end
  end,
  onPageScrollStateChanged = function(state)
  end;
};

function 功能1.onClick()
  pg.showPage(0);

end
function 功能2.onClick()

  pg.showPage(1);
end
function 功能3.onClick()

  pg.showPage(2);
end

function 功能4.onClick()

  pg.showPage(3);
end
```
