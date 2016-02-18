## 4.3 控件
### 4.3.1 活动指示器
活动指示器表明任务或进程正在进行中，如下图所示。

![](images/40.png)

API 注释

想要了解如何在代码中定义活动指示器，可以参考 [UIActivityIndicatorView Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityIndicatorView_Class/index.html#//apple_ref/doc/uid/TP40006830).

活动指示器：

- 当任务进行和加载时旋转，任务完成后自动消失
- 不支持用户交互行为
在工具栏或主视图中使用活动指示器来告知用户任务或加载正在进行中，但并不提示该过程何时会结束。

**不要使用静止的活动指示器。**用户会以为该进程停滞了。

**用活动指示器来让用户知道进程仍在进行中。**有些时候，告诉用户进程没有停止比告诉他们何时完成更加重要。

**设计一个与应用的风格协调的活动指示器。**可以的话，让活动指示器的尺寸和颜色与它所在的背景协调。

### 4.3.2 添加联系人按钮
添加联系人按钮让用户将现有联系人添加到文本框或者其它文字视图中。

![](images/41.png)

API 注释

想要了解如何在代码中定义添加联系人按钮，请参考 [UIButton](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIButton_Class/index.html#//apple_ref/occ/cl/UIButton).

添加联系人按钮：

- 展示联系人列表
- 帮助用户将一个联系人添加到当前联系人按钮所在的视图中
使用添加联系人按钮让用户在不需要使用键盘的情况下就可以方便地访问到联系人。举个例子，在新建邮件的界面中，用户可以点击该按钮来在邮件中添加收件人，而不需要用键盘输入收件人的名字。

由于添加联系人按钮属于键盘输入联系人方法的替代品，我们不推荐在不支持键盘输入的界面中使用添加联系人按钮。

### 4.3.3 日期时间选择器
日期时间选择器展示关于日期和时间的组件，比如小时，分钟，天，以及年。

![](images/42.png)

API 注释

想要了解如何在代码中定义添加日期时间选择器，请参考 UIDatePicker.

日期时间选择器：

- 最多可以展示4个独立的滑轮，每一个滑轮表示一个不同的值，比如月份或小时等
- 在每个滑轮的中央使用深色字体来表示当前选中的值
- 日期时间选择器的大小与 iPhone 键盘的大小相同，并且不可更改
- 包括四种模式，每一种模式代表了一组不同的值:
- **日期和时间**。日期和时间模式（默认模式）包含日期、小时、和分钟，以及一个可选的AM/PM值。
- **时间**。时间模式包括小时和分钟，以及可选的 AM/PM 值。
- **日期**。日期模式包括月份，天以及年三个值。
- **倒计时器**。倒计时器模式展示了小时和分钟值。你可以精确地设定总共的倒计时间，倒计时的最大值为23小时59分钟。
使用日期时间选择器来让用户选择时间，而不是让用户自己输入一个包含了日期、时间等多个部分的时间值。

**尽量地让用户在当前内容中使用日期选择器。**尽量地让用户在当前内容中使用日期选择器。最好避免用户在使用日期选择器的时候要进入另外一个界面。在水平方向的常规环境，日期时间选择器可能会出现在一个浮层中，或者嵌入在当前内容里。

**有必要的时候，改变分钟滑轮的单位刻度。**在默认情况下，分钟滑轮包含从0到59共60个值，如果你要展示一个颗粒度较大的时间，你可以让分钟滑轮的单位刻度变大，只要这个刻度可以整除60。比如说你可能会设定每15分钟为一个刻度，此时分钟滑轮就有4个值，0、15、30、45。

### 4.3.4 详情展开按钮
详情展开按钮展示了与该项相关的更多详细信息与功能描述。

![](images/43.png)

API 注释

想要了解如何在代码中定义详情展开按钮，可以参考 [UITableViewCell Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/index.html#//apple_ref/doc/uid/TP40006938) 和 [UIButton](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

详情展开按钮以一个单独的视图展示特定项目的更多详情信息与功能。

当详情展开按钮在表格行中出现时，点击表格行的其它区域不会激活此按钮，只会选中该行，或者触发 app 中其它自定义的行为。

一般来说，你会在一个表格视图中使用详情展开按钮来让用户知道更多关于这个列表项的信息。当然你也可以将这个按钮用在其它类型的视图中来为用户展示更多与特定项目相关的信息和功能。

### 4.3.5 信息按钮
信息按钮展示了 app 的配置信息，有时候它会出现在当前视图的背面。

![](images/44.png)

API 注释

想要了解如何在代码中定义信息按钮，可以参考 [UIButton](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

iOS 包含了两种信息按钮样式：适用于浅色内容上的深色按钮，以及适用于深色内容上的浅色按钮。

使用信息按钮来显示 app 的配置信息或选项。你可以根据自己 app 的 UI 风格来选择最为协调的信息按钮样式。

### 4.3.6 标签
标签用于放置静态文本。

![](images/45.png)

API 注释

想要了解如何在代码中定义标签，可以参考 [UILabel Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UILabel_Class/index.html#//apple_ref/doc/uid/TP40006797).

标签可以：

- 展示任意数量的静态文本
- 禁止除了复制文本外的任何用户交互行为
你可以使用标签来命名或解释你的部分 UI，又或者用它来给用户提供一些简单的信息。标签最适合拿来展示相对简单的文本信息。

**保证你的标签清晰易读。**最好支持动态文本(Dynamic Type)，并使用 [UIFont](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIFont_Class/index.html#//apple_ref/occ/cl/UIFont) 中的 preferredFontForTextStyle 来获得标签中的展示文本。如果你要用自定义字体的话，请慎重选择字体种类，不要以牺牲清晰度为代价来换取花哨的颜色和字体效果。（想要了解关于app中字体使用的指南，可以参考 [Color and Typography](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ColorImagesText.html#//apple_ref/doc/uid/TP40006556-CH58-SW1);想要了解更多动态文本的内容，可以参考 [Text Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009542) 里面 的 [Text Styles](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/CustomTextProcessing/CustomTextProcessing.html#//apple_ref/doc/uid/TP40009542-CH4-SW65) 部分。）

### 4.3.7 网络活动指示器
网络活动指示器在状态栏中出现，表示网络活动正在进行。

![](images/46.png)

API 注释

你可以在代码中使用 UIApplication 的 [networkActivityIndicatorVisible](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html#//apple_ref/occ/instm/UIApplication/isNetworkActivityIndicatorVisible) 来控制该活动指示器的可见性。

网络活动指示器：

- 出现在状态栏中，当网络活动正在进行时它会旋转，在活动停止时它则消失
- 不支持用户交互行为
当你的 app 正在链接网络，而这个连接过程将会持续好几秒的时候，你可以通过网络活动指示器来给用户以反馈。如果进程所需时间很短，则不需要用到它，因为很可能在用户注意到它之前，它就消失了。

### 4.3.8 页面控件
页面控件告诉用户当前共打开了多少个视图，还有他们正处在其中哪一个。

![](images/47.png)

API 注释

想要了解如何在代码中定义页面控件，可以参考 [UIPageControls](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPageControl_Class/index.html#//apple_ref/occ/cl/UIPageControl).

页面控件：

- 包含一系列圆点，圆点的个数代表了当前打开的视图数量（从左到右，这些圆点代表了视图打开的先后顺序）
- 默认情况下，使用不透明点来标识当前打开的视图，使用半透明点来表示所有其它视图
- 不支持用户访问不连续的视图
- 当视图数量超过页面宽度可承载的氛围时，点的大小和间距并不会因此变小（如果需要显示的点超过一定数量，系统会把它截断）
- 默认情况下不支持视图之间导航；你必须实现视图到视图之间的导航并适当地更新页面控件状态
当告知用户有多少打开的视图的需求比帮助用户选择特定的视图更重要时，使用页面控件。页面控件是为所有视图均平等的场景而设计的。

**不要使用页面控件来显示视图中的层次结构或其他复杂的排列。**页面控件不显示视图是如何相互关联的，而且不表明哪个视图对应于每个点，因此它不能帮助用户导航到特定的视图。

**避免显示太多点。**超过10个点就很难让用户一目了然，而超过20个视图在序列中访问起来非常耗时。如果用户可以在你的应用程序打开超过20个视图，请考虑给视图一个不同的展示方式，以提供关于视图的详细信息，使其支持不连续的导航。

**在打开视图的底部边缘和屏幕的底部边缘里垂直居中页面控件。**在这个位置，页面控件是始终可见的，并且不会阻挡用户的使用。

### 4.3.9 选择器
选择器展示了一组值，用户可以从中选择一个。

![](images/48.png)

API 注释

想要了解如何在代码中定义选择器，可以参考 [UIPickerView Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPickerView_Class/Reference/UIPickerView.html#//apple_ref/doc/uid/TP40006842).

选择器：

- 是日期时间选择器的通用模式
- 包括一个或多个滑轮，每个滑轮含有一组值
- 当前选中的值在中间，以深色标识
- 不可以自定义大小（选择器的大小与 iPhone 的键盘相同）
使用选择器可以让用户更容易从一系列不同的值中间进行选择。

**一般来说，当用户对整组值都比较熟悉的时候，可以使用选择器。**由于当滑轮静止的时候，大部分的数值会被隐藏，最好是在用户对所有数值均有预期的情况下才使用选择器。当你需要展示一大组用户并不熟悉的选项，此种选择器可能不太适合。

**尽可能让让用户在当前视图中使用选择器。**不要让他们在使用选择器时还要进入其它的视图。

**如果你需要展示的备选项数量很多，考虑使用表格视图(Table View)而不是选择器。**因为表格视图的高度较大，内容滚动起来会更快。

### 4.3.10 进度视图
进度视图展示了任务或进程的进度（下图是 iOS 默认邮件 App 的工具栏）。

![](images/49.png)

API 提示：

想要了解更多如何在代码中定义进度视图，可以参考 [UIProgressView Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIProgressView_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006782).

进度视图：

- 是一条轨迹，随着进程的进行从左向右进行填充
- 不支持用户交互行为
iOS 定义了两种进度视图样式：

- **默认(Default)**.默认样式适合用在 app 的主要内容区中。

![](images/50.png)

- **进度条(Bar)**.此样式比默认样式细，适合用在工具栏中。

![](images/51.png)

当一个任务存在明确的进程，可以使用进度条来给与用户反馈，尤其在需要明确告诉用户这个任务大约需要多少时间完成的时候。

**可以的话，请根据你的 app 的风格来设计进度条的外观。**你可以自定义进度条的底色以及轨迹颜色，也可以直接使用图片。

### 4.3.11 刷新控件
刷新控件执行用户触发的内容刷新——一个典型的例子，它常在表格中出现（下图展示的是 iOS 默认的邮件 app 的 mailbox 列表页）。

![](images/52.png)

API 提示：

想要了解更多如何在代码中定义刷新控件，可以参考 [UIRefreshControl Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIRefreshControl_class/Reference/Reference.html#//apple_ref/doc/uid/TP40012250).

刷新控件：

- 看起来类似活动指示器
- 可以出现在标题中
- 默认状态下不可见，当用户在表格上缘往下拖拽以刷新内容时才出现
使用刷新控件，给用户提供一个一致的方式来了解一个表格或其他视图的内容更新，而不需要等待下一个自动更新。

**就算你使用了刷新控件，也不要因此就不支持内容自动刷新。**尽管用户喜欢在执行刷新操作时内容立刻刷新，他们也同样会喜欢内容自动刷新。如果过于一来用户自己执行所有刷新操作的话，那些不会自动刷新的用户就会疑惑，为何你 app 中的数据永远都不更新。一般来说，刷新控件给了用户多一个选择，让他们可以立刻获得最新的内容，但同时，你也不能奢望用户会主动获取所有的更新信息。

**只有在必要的时候才加短标题。**特别需要注意的是，不要使用短标题来描述刷新控件怎么使用。

### 4.3.12圆角矩形按钮
iOS7 及更新版本中已经不再使用圆角矩形按钮，而是使用了新的系统按钮——类型为 UIButtonTypeSystem 的 UI 按钮 ([UIButton](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIButton_Class/UIButton/UIButton.html#//apple_ref/occ/cl/UIButton)) 。使用指南可参考 [System Button](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW10).

### 4.3.13 分段控件
分段控件是一组分段的线性集合，每一个分段的作用类似按钮，点击之后将切换到相应的视图。

![](images/53.png)

API 提示：

想要了解更多如何在代码中定义分段控件，可以参考 [Segmented Controls](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UISegmentedControl.html#//apple_ref/doc/uid/TP40012857-UISegmentedControl)

分段控件：

- 由两个或以上的分段组成，每一个分段的宽度相同，与分段的数量成比例（分段数量越多，则宽度越小）
- 可以包含文字或者图片
使用分段控件来提供密切相关而又互斥的选项。

**保证每个分段都容易点击。**为了保证每个分段的大小有至少44×44像素，请控制分段的数量。在 iPhone 上，1个分段控件最多包含5个分段。

**尽可能地保持每个分段中的文字长度一致。**因为每个分段都是等宽的，当文本长度差异很大时看上去会很不协调。

**不要在同一个分段控件中混用文字和图片。**每一个分段都仅可支持纯文字或纯图片。避免在同一个分段控件中，一些分段里使用纯文字，另一些分段里使用纯图。

**请在必要时调整分段控件中文本的对齐方式。**如果你给分段控件添加了自定义底图，请确保控件里自动居中的文本依然清晰美观。你可以通过 bar metrics APIs 来调整分段控件内文本的对齐方式(想要了解如何定义 bar metrics，可以参考 [UISegmentedControl](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISegmentedControl_Class/index.html#//apple_ref/occ/cl/UISegmentedControl) 中关于自定义 API 外观(appearance-customization APIs)的描述)。

### 4.3.14 滑块
滑块允许用户在一个限定范围内调整某个数值或进程(下图展示的是 iOS 设置中亮度设置的滑块，滑块的左边和右边均为自定义图形)。

![](images/54.png)

API 提示：

想要了解更多如何在代码中定义滑块，可以参考 [Sliders](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UISlider.html#//apple_ref/doc/uid/TP40012857-UISlider)

滑块：

- 由一条水平的轨迹和一个 Thumb(滑块中支持用户水平拖拽的圆形控件)组成
- 左边和右边支持使用自定义图片来表述相对的最小值与最大值的含义
- 填充轨道左边缘最小值之间到 Thumb 之间的部分
使用滑块来让用户精准地选择自己想要的值，或者控制当前的进程。

**如果合适的话，自定义滑块的外观。**比如，你可以:

- 定义 Thumb 的外观，让用户一看就知道滑块当前的状态
- 在轨迹的左右两端使用自定义图片来告诉用户滑块的最小值和最大值所代表的含义。比如说，一个图调整图片尺寸的滑块可以在最小值的左边放一张小图，在最大值的右边放一张大图。
- 根据 Thumb 所在的位置和当前滑块的状态来为滑块的轨迹定义不同的颜色
**不要使用滑块来显示音量控制。**如果你需要显示一个音量滑块，当你使用 [MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView) 类的时候请使用系统提供的音量滑块。请注意，当当前活动的音频输出设备不支持音量控制时，音量滑块以适当的设备名称替换。

### 4.3.15 步进器
步进器可以以常数为幅度来增减当前数值。

![](images/55.png)

API 提示：

想要了解更多如何在代码中定义步进器，可以参考 [UIStepper](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UIStepper.html#//apple_ref/doc/uid/TP40012857-UIStepper).

步进器：

- 是一个两段控件，其中一段默认显示减号，另一端默认显示加号
- 支持自定义图片
- 不展示用户更改的值
当用户想要对数值进行小幅度调整时，可以使用步进器。

**当用户需要大幅度调整数值的时候，不要使用步进器。**用户可能会在打印机里使用步进器来确定打印份数，因为这个值的变化幅度通常并不大；而当用户需要选择打印的页码范围时，使用步进器就会让操作变得繁琐，因为用户很可能要点很多下才能选定页数。

**确保步进器所调整的值明显可见。**步进器自身不展示任何数值，所以你需要保证让用户知道他们正在调整哪一个数值。

### 4.3.16 开关按钮
开关按钮展示了两个互斥的选项或状态。

![](images/56.png)

API 提示：

想要了解更多如何在代码中定义步开关，可以参考 [UISwitch](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UISwitch.html#//apple_ref/doc/uid/TP40012857-UISwitch).

开关按钮：

- 显示了一个项存在二元状态
- 仅在表格视图中可用
在表格中使用开关按钮来让用户从某一项的两个互斥状态中指定一个，比如是/否(Yes/No)，开/关(On/Off)。

你可以使用开关按钮来控制视图中的其它 UI 元素。根据用户的选择，新的列表项可能出现或者消失，或从激活状态变为不激活状态。

### 4.3.17 系统按钮
系统按钮执行 app 中定义的行为。

![](images/57.png)

API 提示：

在 iOS 7 中，UIButtonTypeRoundedRect 已经被重新定义为 UIButtonTypeSystem. 想要了解更多如何在代码中定义系统按钮，可以参考 UIButton.

系统按钮：

- 默认状态下不含边界，也不含背景图
- 可以是图标或者文字标题
- 支持自定义样式，如描边或者加背景图(想要自定义按钮外观，可以使用 UIButtonTypeCustom 类型的按钮，并且提供背景图片)
使用系统按钮来执行某个动作。当你为系统按钮命名时，请遵循以下方法：

- **使用动词或动词短语来描述按钮所代表的动作**。这种命名方法告诉用户这个按钮是可交互的，也提示了用户点击之后会执行什么操作
- **使用标题式大写**(title-style capitalization，每个单词的首字母均大写)。除了冠词，并列连词以及少于4个字母的介词外，标题中每个单词的首字母均大写。
- **标题不要太长**。太长的标题会被截断，让用户难以理解其含义
以 iPhone 为例，给数字按键添加圆形边框强化了用户拨电话号码时的心理模型，而结束(End)和隐藏(Hide)按钮的背景色让用户拥有了更大的点击范围。

**合适的话，为内容区域内的系统按钮描边或者加入背景。**大多数情况下，你可以通过定义一个清晰的按钮名称、选择一个不一样的标题颜色或提供上下文情景提示来让用户知道这是一个按钮而非普通文本。但在某些特定的内容区域内，为按钮描边或者添加背景颜色，让用户迅速地把注意力放到按钮上，也是必要的。Value 2 的布局中，文本和副标题中间的垂直间距会让用户专注于副标题的第一个单词。

![](images/58.png)

### 4.3.18文本框
开关按钮展示了两个互斥的选项或状态。

![](images/59.png)

API 提示：

想要了解如何在代码中定义文本框，以及在文本框中支持图片和按钮，可以参考 [UITextField](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextField_Class/index.html#//apple_ref/occ/cl/UITextField).

文本框

- 高度固定，包含圆角
- 当用户点击它时，自动唤起输入键盘
- 可以包含系统提供的按钮，如书签按钮(Bookmarks)
- 可以展示多种文字样式(了解更多请参考 [UITextView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextView_Class/Reference/UITextView.html#//apple_ref/occ/cl/UITextView))
使用文本框来获取用户输入的少量信息。

**你可以自定义一个文本框，帮助用户更好地理解如何使用它。**举个例子，你可以在文本框的左侧或者右侧加入自定义图形，或者加入系统按钮，如书签按钮等。一般来说，文本框的左侧用于表述文本框的含义，而右侧用于展示附加的功能，如书签。

**合适的话，在文本框右侧加入清除按钮。**轻击清除按钮变可清空当前框内输入的全部内容，无论你原本打算在这个按钮上面展示什么其它图片。

**如果可以帮助用户理解的话，可以在文本框中加入提示文字。**当文本框里没有任何其它提示文字时，会展示占位符文本(placeholder text)，如名字、地址等。

**根据输入内容的类型来指定不同的键盘类型。**举例来说，你希望用户能更方便地输入网址、密码或者电话号码。iOS 提供了各种不同的键盘类型，以便用户输入不同类型的文本。想要了解可用键盘类型，可以参考 [UITextInputTraits Protocol Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextInputTraits_Protocol/index.html#//apple_ref/c/tdef/UIKeyboardType) 中的 [UIKeyboardType](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextInputTraits_Protocol/index.html#//apple_ref/c/tdef/UIKeyboardType).想要了解如何在管理你的应用中的键盘，请参考 [Managing the Keyboard](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/KeyboardManagement/KeyboardManagement.html#//apple_ref/doc/uid/TP40009542-CH5) 部分。但请注意，由于键盘的布局以及输入方法是由用户的系统语言设置决定的，这是你不能控制的。