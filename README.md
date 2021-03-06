在消金企业里，最核心的运作部门主要是营销、风控以及产品。营销和风控：两者既对立又互相依赖，若没有足够的客户，风控便无法发挥作用，而有了坚实的风控后盾，才能可持续的拓展业务并维护下去。而产品部门则是结合现有客群以及辅助风控部门，制定规则、调整产品，定义目标客群。

简单来说，消费金融的风控就是对客户不还钱的可能性做侦查、判断并对其管控。需要考虑的就是这个客户的还款能力、还款意愿以及公司的政策松紧。所涉及的风控的维度及数据由于不同的公司的客户来源、业务内容、风控流程都不尽相同，根据需要来选定。这里主要从业务层，按贷前中后讲一些通用的内容。






贷前（进件）

信息提交、核验
首先是客户的基本信息获取：如银行卡四要素/运营商三要素等；同时收集一些额外的信息，根据业务需要设定必要提供或自愿提供的信息，用于后续的风控流程。
除了信息提交完整外，还需对真实性做交叉验证：如姓名、手机登记的姓名、身份证是否一致， ip地址与客户消费场景所在地是否一致，活体检测、OCR识别、与公安系统对比等。

申请反欺诈
这一步说白了就是将一些风险较高、资质较差的客户设立门槛，拦截在外，那么技术人员需知道 的就是：设哪些门槛、设多高、怎么设？
考虑到时间方面的效率，以及财务上的成本，一般先以比较直接的规则拦截，然后再走模型，而 使用的数据也根据成本递增，优先以0成本的数据拒件，避免不必要的开支。

（1）准入规则
1.合规方面不符合的人群：如不接受未成年、学生的贷款；
2.非目标的客群：如助农贷只对农民，医美贷不对老人等；
3.反欺诈规则：黑名单、身份伪冒、多头借贷、征信不良等；
4.其他

（2）反欺诈评分卡模型
根据实际需要，也可使用反欺诈评分卡模型，补足完善或代替直接以反欺诈规则拒件。

贷前的反欺诈评分主要考虑：有无设备被盗风险；有无可能薅羊毛、撸贷；有无身份造假、信息伪造；是否特殊身份如信贷中介、羊毛党、社交白户等；是不是团伙欺诈……

A、所需特征：
1.基本信息（身份证、手机号、地址、公司……）
2.设备相关（关联多手机号、关联多用户、手机关联过多设备）
3.ip相关（ip异常）
4.团伙相关（一、二度联系人）
5.通话详单/通讯录（若是交易性联系，次数会很少）
6.外部资信如征信记录、三方黑名单等
7.三方欺诈数据（如同盾分）
8.异常检测数据（如授权过于频繁、申请地理位置/时间异常）

B、交叉验证：
尽可能利用已有的信息，
1.抓出客户个人的矛盾点：如手机号绑定身份与身份证不一致、公司所在地与ip不一致、微信支 付宝绑定手机号与申请手机号不一致、支付宝姓名与身份证不一致等；
2.抓出客户之间的共同点：自填信息较多雷同、短期内一批用户共同信息高度相同等；
3.交叉得出高风险：联系人中有存在黑名单、与问题客户或中介一度二度关联；
4.排除因业务类型、目标客群等导致的特征共性，以免错误判断。

申请评分卡模型
以申请者在申请当日及过去的信息为基础，预测未来放款后的逾期或者违约的概率。
反欺诈评分卡和申请评分卡的区别：申请评分卡更多的是衡量客户的还款能力；反欺诈评分卡更多的是衡量客户的还款意愿。
反欺诈评分模型不是必须的，两者所采用的变量也没有说不能重复。

一般需要以下字段
1.个人信息：学历、性别、收入、工作等；
2.负债能力：负债情况，多头信息等； 
3.消费能力：商品购买记录，出境游，奢侈品消费等； 
4.历史信用记录：征信记录、三方逾期等； 
5.其他数据：个人交际、网络足迹、个人财务等； 

关于阈值
方法1：以不同阈值代入样本验证讨论
方法2：从收益和风险的平衡考虑
方法3：结合经验及业务需要

额度授信
这一步就是要评估这个客户最多可以从我们平台贷多少金额
1.结合产品类型及公司策略，设定最高和最低的额度；
2.选定还款能力、风险程度等类型的考核的指标；
3.拟出初始额度；
4.调整最优额度。

人工审核
某些情况下：如技术还不够成熟，或者客群量还不够大，或者业务所需，还需配合人工审核进一步判断，常见的形式为征信电话。

人工主要对以下方面做了解判断：1.真实性（身份的真实性、自填资料的真实性）；2.贷款用途、还款计划；3.个人的基本情况（如工作、收入、家庭等）；4.其他（如消费习惯等）



贷中
  
跟踪回访/交易监控
贷中正常回访：以官方身份电联客户，向客户做信息搜集、基本确认交易真实性、判断风险情况以及还款意愿，同时也是对客户关系的维护。对纠纷类客户做好安抚工作，降低对还款意愿的影响。

交易反欺诈
线上产品：需检测是否存在刷单行为、确认商品本人收货使用；
线下产品：如车贷、医美等，需确保交易公平自愿，服务类需本人消费并提供消费凭证；
如果培训、租房、医美等，此类场景风险还需考虑B端，需确保商户的经营资质、持续经营能力。

关于反欺诈的策略，假使已经有足够样本，可做验证：逾期、高额、年龄、地区、社交图谱、学历等，分别击中率是多少，赋予不同权重。

1.行为评分卡模型
已经放出贷款以后，根据贷款人的消费习惯，还款情况等一些信用特征，跟踪客户的表现，来预估用户逾期或者是违约概率

主要涉及到月还款率变量、额度使用率变量、逾期率变量、消费类型、三方数据等。

2.尽职调查
由于欺诈形式多变，层出不穷，有时还需前往一线对实际情况做了解，根据所得经验对其做填补。
A、通过客户提供的一些基本资料、银行征信报告、利用公司内部的信贷管理系统、电话、网络媒体（如工商网、社保网）等工具或渠道进行信息收集、分析等检查
B、实地走访客户，与客户的面谈，核实工作单位等；如果有B端消费场景，那么还可以前往考察，了解运作模式，获客来源等
C、与客户、商家、中间介绍人联系，了解是否存在（潜在的）欺诈风险；与上面区别在于如有需要可稍作变通，如以非官方的身份暗访了解
D、欺诈套现这一块涉及黑灰产较多，甚至有不少中介对信贷、反欺诈方面做足了功课，知晓银行及各贷款公司的规则，懂得应变，当黑产以摸索清楚规律而在其中自由游走时，我们的防护就会让风险有机可乘，所以需要在黑产行动之前，先行做好预防工作。具体的措施是可以去相关的贴吧、论坛、社交群中获取相关的信息。

二次营销
客户的还款周期大部分都是一年以上，期间电话回访或者软件界面、公众号广告吸引等，都可以
吸引客户二次消费，这么做既降低流量的浪费，老客的风险也相对较低，一举二得。



贷后

商账管理
在赊销业务中，保证足额、及时收回应收账款，以降低和避免资金周转、坏帐损失等弊端。对于
贷了款却由于各种原因不想使用的客户，及时收回，可有效减少商账的周期。

催收
（1）催收流程
通常的流程大致如下 ：还款前短信提醒→逾期初短信提醒→逾期初电话提醒→逾期初电话催收→实地文明催收→法院→外包

其中：前期的短信提醒及初期的电话提醒都可以以机器人批量处理，后期的电话催收如有需要也可以安排机器人质检，这么做可以节省时间和人力。

（2）催收评分卡模型
对已逾期或者违约的客户，进行一个催收评分，分别为还款率模型，账龄滚动模型，失联模型。

还款率预测模型：预测经催收后，最终收回的欠款的比率；

账龄滚动模型：预测逾期人群从轻度逾期发展至重度逾期的概率；

失联模型：在逾期阶段，对于尚能联系到的人群预测其未来失联的概率。

常用指标包括：逾期天数、逾期金额、历史还款率、个人信息、联系人关系、运营商信息等

常用的风控指标介绍
[vintage]
按账龄的长短同步对比，了解同一产品不同时期放款的资产质量情况。将不同时期数据拉平到同一时期比较，可直观地比较和反思不同时期公司的营销策略的效果。

[迁移率]
即处于某一逾期阶段的客户转到其他逾期阶段的变化情况。如未逾期为M0，逾期1~29天为M1，以此类推，M2-M3即从逾期阶段为M2转到M3的比例。迁移率通常可以用来预测不同逾期阶段的未来坏账损失。

[滚动率]
以某一时间点为观察节点，观察客户在该点前一段时间内最坏逾期阶段，并追踪其在观察点之后的一段时间向其他逾期阶段发展的情况，特别是向更坏程度发展的情况。vintage是从时间维度上判断客户群体的好坏，滚动率则是从行为程度上判断客户的好坏，它可以帮助我们判断某些逾期客户是否还可以再抢救一下，收回点成本。

[入催率]
指的是在某一个还款日，客户从M0变成M1的比例。例如今天有N个M0客户到了还款日，里面有M个客户按时还款了，那么今天的入催率就是（N-M）/N

[首逾率]
在某一个还款日，仅第一期到期的客户中有多少没有按时还款。与入催率的差别在于，入催率包含了第一期、第二期、第三期等等所有到期的M0。该指标一般用于反欺诈，因为欺诈客户经常一期都不还。 
