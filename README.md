# DecryptPrompt
> 如果LLM的突然到来让你感到沮丧，不妨读下主目录的Choose Your Weapon Survival Strategies for Depressed AI Academics
持续更新以下内容，Star to keep updated~
1. 开源LLM
2. 指令微调和RLHF数据以及训练框架
3. Prompt和LLM相关论文按细分方向梳理
4. AIGC相关应用
5. Prompt指南和教程
6. ChatGPT及AGI相关解读

## My blogs & ChatGPT应用
- [解密Prompt系列1. Tunning-Free Prompt：GPT2 & GPT3 & LAMA & AutoPrompt](https://cloud.tencent.com/developer/article/2215545?areaSource=&traceId=)
- [解密Prompt系列2. 冻结Prompt微调LM： T5 & PET & LM-BFF](https://cloud.tencent.com/developer/article/2223355?areaSource=&traceId=)
- [解密Prompt系列3. 冻结LM微调Prompt: Prefix-tuning & Prompt-tuning & P-tuning](https://cloud.tencent.com/developer/article/2237259?areaSource=&traceId=)
- [解密Prompt系列4. 升级Instruction Tuning：Flan/T0/InstructGPT/TKInstruct](https://cloud.tencent.com/developer/article/2245094?areaSource=&traceId=)
- [解密prompt系列5. APE+SELF=自动化指令集构建代码实现](https://cloud.tencent.com/developer/article/2260697?areaSource=&traceId=)
- [解密Prompt系列6. lora指令微调扣细节-请冷静,1个小时真不够~](https://cloud.tencent.com/developer/article/2276508)
- [解密Prompt系列7. 偏好对齐RLHF-OpenAI·DeepMind·Anthropic对比分析](https://cloud.tencent.com/developer/article/old/2289566?areaSource=&traceId=)
- [解密Prompt系列8. 无需训练让LLM支持超长输入:知识库 & Unlimiformer & PCW & NBCE ](https://cloud.tencent.com/developer/article/old/2295783?areaSource=&traceId=)
- [解密Prompt系列9. 模型复杂推理-思维链基础和进阶玩法](https://cloud.tencent.com/developer/article/old/2296079?areaSource=&traceId=)
- [解密Prompt系列10. 思维链COT原理探究](https://cloud.tencent.com/developer/article/old/2298660)
- [ChatGPT应用1. MakeInstruction零人工指令样本构建](https://huggingface.co/spaces/xl2533/MakeInstruction)
- [ChatGPT应用2. ChatPDF简单复现](https://huggingface.co/spaces/xl2533/FinDoc)


## 模型和数据
- [可商用LLM列表](https://github.com/eugeneyan/open-llms)
- [CMU开源聊天机器人评测应用](https://github.com/zeno-ml/zeno-build): ChatGPT>Vicuna>others；在对话场景中训练可能很重要
- [Berkley出品大模型排位赛榜有准中文榜单](https://lmsys.org/blog/2023-05-03-arena/): GPT4自然是稳居第一，GPT4>Claude>GPT3.5>Vicuna>others
- [Z-Bench中文真格基金评测](https://github.com/zhenbench/z-bench): 国产中文模型的编程可用性还相对较低，大家水平差不太多，两版ChatGLM提升明显
- [Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard): 在Eleuther AI4个评估集上评估的LLM模型榜单
- [Chain-of-thought评估](https://github.com/FranxYao/chain-of-thought-hub):GSM8k, MATH等复杂问题排行榜

### 国外模型
|模型链接     | 模型描述    |
| --- | --- |
| [Google Bard](https://bard.google.com)   |    谷歌bard虽迟但到，可以申请waitlist了 |
|  [Claude](https://www.anthropic.com/product)   |  ChatGPT最大竞争对手Claude也开放申请了，slack中无限试用   |
|  [Falcon](https://huggingface.co/tiiuae/falcon-40b)   |  Falcon由阿联酋技术研究所在超高质量1万亿Token上训练得到1B，7B，40B开源，免费商用！土豪们表示钱什么的格局小了 |
| [LLaMA](https://github.com/facebookresearch/llama)    |  Meta开源指令微调LLM，规模70 亿到 650 亿不等  |
|[MPT](https://huggingface.co/mosaicml/mpt-7b-chat)|MosaicML开源的预训练+指令微调的新模型，可商用，支持84k tokens超长输入|
|[RedPajama](https://huggingface.co/togethercomputer/RedPajama-INCITE-Instruct-3B-v1)|RedPajama项目既开源预训练数据后开源3B，7B的预训练+指令微调模型|
|[ChatLLaMA](https://github.com/nebuly-ai/nebullvm/tree/main/apps/accelerate/chatllama)     | 基于RLHF微调了LLaMA     |
| [Alpaca](https://github.com/tatsu-lab/stanford_alpaca)    |  斯坦福开源的使用52k数据在7B的LLaMA上微调得到，   |
|[Alpaca-lora](https://github.com/tloen/alpaca-lora)     |   LORA微调的LLaMA  |
|[Dromedary](https://github.com/IBM/Dromedary)|IBM self-aligned model with the LLaMA base|
|[Vicuna](https://github.com/lm-sys/FastChat)|Alpaca前成员等开源以LLama13B为基础使用ShareGPT指令微调的模型，提出了用GPT4来评测模型效果|
|[koala](https://bair.berkeley.edu/blog/2023/04/03/koala/)|使用alpaca，HC3等开源指令集+ ShareGPT等ChatGPT数据微调llama，在榜单上排名较高|
|[ColossalChat](https://github.com/hpcaitech/ColossalAI)|HPC-AI Tech开源的Llama+RLHF微调|
|[MiniGPT4](https://github.com/Vision-CAIR/MiniGPT-4)|Vicuna+BLIP2 文本视觉融合|
|[StackLLama](https://huggingface.co/trl-lib/llama-7b-se-rl-peft)|LLama使用Stackexchange数据+SFT+RL|
|[Cerebras](https://huggingface.co/cerebras/Cerebras-GPT-13B)|Cerebras开源了1亿到130亿的7个模型，从预训练数据到参数全开源|
|[PaLM-E](https://palm-e.github.io)     |  谷歌多模态大模型，540B的PaLM语言模型和22B的ViT视觉模型相结合，得到562B的PaLM-E模型，在机器人应用场景有了新的突破   |
|[Dolly-v2](https://huggingface.co/databricks/dolly-v2-7b)|可商用 7b指令微调开源模型在GPT-J-6B上微调|
|[OpenChatKit](https://github.com/togethercomputer/OpenChatKit)|openai研究员打造GPT-NoX-20B微调+6B审核模型过滤|
|  [MetaLM](https://github.com/microsoft/unilm)    | 微软开源的大规模自监督预训练模型    |
|[Amazon Titan](https://aws.amazon.com/cn/bedrock/titan/)|亚马逊在aws上增加自家大模型|
| [OPT-IML](https://link.zhihu.com/?target=https%3A//github.com/facebookresearch/metaseq/tree/main/projects/OPT)     |  Meta复刻GPT3，up to 175B, 不过效果并不及GPT3   |
|[Bloom](https://huggingface.co/bigscience/bloom)|BigScience出品，规模最大176B|
|[BloomZ](https://huggingface.co/bigscience/bloomz)|BigScience出品, 基于Bloom微调|
|[Galacia](https://github.com/paperswithcode/galai)|和Bloom相似，更针对科研领域训练的模型|
| [T0](https://github.com/bigscience-workshop/t-zero)|BigScience出品，3B~11B的在T5进行指令微调的模型|

### 国内模型
|模型链接     | 模型描述    |
| --- | --- |
|  [ChatGLM](https://github.com/THUDM/ChatGLM-6B)   |     清华开源的、支持中英双语的对话语言模型，使用了代码训练，指令微调和RLHF。和以下GLM相同大小的130B的模型还在开发中。试用了下超出预期！|
|  [Moss](https://github.com/OpenLMLab/MOSS)   |  为复旦正名！开源了预训练，指令微调的全部数据和模型。可商用 |
|[Wombat-7B](https://huggingface.co/GanjinZero/wombat-7b-delta)|达摩院开源无需强化学习使用RRHF对齐的语言模型, alpaca基座|
|[TigerBot](https://github.com/TigerResearch/TigerBot)|虎博开源了7B 180B的模型以及预训练和微调语料|
|[Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)     |   哈工大中文指令微调的LLaMA  |
|  [Luotuo](https://github.com/LC1332/Luotuo-Chinese-LLM)   |  中文指令微调的LLaMA，和ChatGLM   |
| [文心一言](https://yiyan.baidu.com/welcome)    |  已经拿到邀请码并试用，虽然人格化程度显著低，但效果上并没有很拉胯，国产YYDS！不过商业化霸王条款确实不少   |
|[通义千问](https://tongyi.aliyun.com/)|阿里系LLM开放申请|
|[星火](https://passport.xfyun.cn/login)|科大讯飞星火，数学是真的厉害|
|[Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)|智源开源7B大模型可商用免费|
|[Baichuan](https://github.com/baichuan-inc/baichuan-7B)|百川智能开源7B大模型可商用免费|
|[BiLLa](https://github.com/Neutralzz/BiLLa)|LLama词表扩充预训练+预训练和任务1比1混合SFT+指令样本SFT三阶段训练|
|[Phoenix](https://github.com/FreedomIntelligence/LLMZoo)|港中文开源凤凰和奇美拉LLM，Bloom基座，40+语言支持|
|[OpenBuddy](https://github.com/OpenBuddy/OpenBuddy)|Llama 多语言对话微调模型|
|[Guanaco](https://huggingface.co/KBlueLeaf/guanaco-7B-leh)|LLama 7B基座，在alpaca52K数据上加入534K多语言指令数据微调|
|[ziya](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-7B-Reward)|IDEA研究院在7B/13B llama上继续预训练+SFT+RM+PPO+HFTT+COHFT+RBRS|
|[Chinese Vincuna](https://github.com/Facico/Chinese-Vicuna)|LLama 7B基座，使用Belle+Guanaco数据训练|
|[Linly](https://github.com/CVI-SZU/Linly)|Llama 7B基座，使用belle+guanaco+pclue+firefly+CSL+newscommentary等7个指令微调数据集训练|
|[Firefly](https://github.com/yangjianxin1/Firefly)| 中文2.6B模型，提升模型中文写作，古文能力，待开源全部训练代码，当前只有模型|
| [Baize](https://github.com/project-baize/baize-chatbot)    | 使用100k self-chat对话数据微调的LLama    |
| [BELLE](https://github.com/LianjiaTech/BELLE)    |使用ChatGPT生成数据对开源模型进行中文优化  |
|[Chatyuan](https://github.com/search?q=chatyuan&type=repositories)|chatgpt出来后最早的国内开源对话模型，T5架构是下面PromptCLUE的衍生模型|
| [PromptCLUE](https://github.com/clue-ai/PromptCLUE)    | 多任务Prompt语言模型    |
| [PLUG](https://www.alice-mind.com/portal#/)    |   阿里达摩院发布的大模型，提交申请会给下载链接  |
|[CPM2.0](https://baai.ac.cn/)     |  智源发布CPM2.0    |
|[GLM](https://github.com/THUDM/GLM-130B) |   清华发布的中英双语130B预训练模型 |

### 垂直领域模型&进展
|模型链接     | 模型描述  
| --- | --- | 
|MedPalm|Google在Faln-PaLM的基础上通过多种类型的医疗QA数据进行prompt-tuning指令微调得到，同时构建了MultiMedQA|
|[ChatDoctor](https://github.com/Kent0n-Li/ChatDoctor)|110K真实医患对话样本+5KChatGPT生成数据进行指令微调|
|[Huatuo](https://github.com/SCIR-HI/Huatuo-Llama-Med-Chinese) [Med-ChatGLM](https://github.com/SCIR-HI/Med-ChatGLM)|医学知识图谱和chatgpt构建中文医学指令数据集+医学文献和chatgpt构建多轮问答数据|
|[Chinese-vicuna-med](https://github.com/Facico/Chinese-Vicuna/blob/master/docs/performance-medical.md)|Chinese-vicuna在cMedQA2数据上微调|
|[OpenBioMed](https://github.com/BioFM/OpenBioMed)|清华AIR开源轻量版BioMedGPT, 知识图谱&20+生物研究领域多模态预训练模型|
|[DoctorGLM](https://github.com/xionghonglin/DoctorGLM)|ChatDoctor+MedDialog+CMD 多轮对话+单轮指令样本微调GLM|
|[MedicalGPT-zh](https://github.com/MediaBrain-SJTU/MedicalGPT-zh)|自建的医学数据库ChatGPT生成QA+16个情境下SELF构建情景对话|
|[PMC-LLaMA](https://github.com/chaoyi-wu/PMC-LLaMA)|医疗论文微调Llama|
|[ NHS-LLM](https://github.com/CogStack/OpenGPT/tree/main)|Chatgpt生成的医疗问答，对话，微调模型|
|[LawGPT-zh](https://github.com/LiuHC0428/LAW-GPT)|利用ChatGPT清洗CrimeKgAssitant数据集得到52k单轮问答+我们根据中华人民共和国法律手册上最核心的9k法律条文，利用ChatGPT联想生成具体的情景问答+知识问答使用ChatGPT基于文本构建QA对|
|[LawGPT](https://github.com/pengxiao-song/LaWGPT)|基于llama+扩充词表二次预训练+基于法律条款构建QA指令微调|
|[Lawyer Llama](https://github.com/AndrewZhe/lawyer-llama)|法律指令微调数据集：咨询+法律考试+对话进行指令微调|
|[LexiLaw](https://github.com/CSHaitao/LexiLaw)|法律指令微调数据集：问答+书籍概念解释，法条内容进行指令微调
|[ChatLaw](https://chatlaw.cloud/)|北大推出的法律大模型，应用形式很新颖类似频道内流一切功能皆融合在对话形式内|
||[FinChat.io](https://finchat.io/)|使用最新的财务数据，电话会议记录，季度和年度报告，投资书籍等进行训练|
|[OpenGPT](https://github.com/CogStack/OpenGPT)|领域LLM指令样本生成+微调框架|
|[乾元BigBang金融2亿模型](https://github.com/ssymmetry/BBT-FinCUGE-Applications/tree/main)|金融领域预训练+任务微调|
|[度小满千亿金融大模型](https://huggingface.co/xyz-nlp/XuanYuan2.0)|在Bloom-176B的基础上进行金融+中文预训练和微调|
|[bondGPT](https://www.ltxtrading.com/bondgpt)|GPT4在细分债券市场的应用开放申请中|
|[IndexGPT](https://www.cnbc.com/2023/05/25/jpmorgan-develops-ai-investment-advisor.html)|JPMorgan在研的生成式投资顾问|
|[恒生LightGPT](https://mp.weixin.qq.com/s/vLvxvi2nOywkjt7ppiFC2g)|金融领域继续预训练+插件化设计|
|[知彼阿尔法](https://finance.sina.com.cn/jjxw/2023-07-03/doc-imyzmaut2132017.shtml)|企查查商查大模型|

### 指令微调&RL工具
| 工具描述   | 链接   | 
| --- | --- | 
|LoRA：Low-Rank指令微调方案|https://github.com/tloen/alpaca-lora|
|peft：parameter-efficient prompt tunnging工具集|https://github.com/huggingface/peft|
|RL4LMs：AllenAI的RL工具|https://github.com/allenai/RL4LMs|
|trl：基于Transformer的强化训练框架|https://github.com/lvwerra/trl|
|trlx：分布式训练trl | https://github.com/CarperAI/trlx|
|北大开源河狸项目可复现RLHF，支持多数LLM，提供RLHF数据|https://github.com/PKU-Alignment/safe-rlhf|
|RL4LMs：AllenAI的RL工具|https://github.com/allenai/RL4LMs|
|LMFlow：港科大实验室开源的大模型微调框架，支持以上多数开源模型的指令微调和RLHF|https://github.com/OptimalScale/LMFlow|
|hugNLP:基于Huggingface开发继承Prompt技术，预训练和是指输入等多种方案|https://github.com/wjn1996/HugNLP|
|Deepspeed：针对RL训练和推理的整合优化|https://github.com/microsoft/DeepSpeed|
|Uerpy:预训练框架支持lm,mlm,unilm等|https://github.com/dbiir/UER-py|
|TecentPretrain: Uerpy的重构版本支持llama预训练|https://github.com/Tencent/TencentPretrain/tree/main|
|lamini: 整合指令数据生成，SFT，RLHF的工具库|https://github.com/lamini-ai/lamini/|
|Chain-of-thought-hub：模型推理能力评估平台|https://github.com/FranxYao/chain-of-thought-hub|
|FlexGen:LLM推理 CPU Offload计算架构|https://github.com/FMInference/FlexGen|
|VLLM：超高速推理框架Vicuna，Arena背后的无名英雄，比HF快24倍|https://github.com/vllm-project/vllm|

### LLM Agent工具

| 工具描述   | 链接   | 
| --- | --- | 
|langchain：LLM工具集|https://github.com/hwchase17/langchain|
|BMTTools: 清华出品类似langchain|https://github.com/OpenBMB/BMTools|
|BabyAGI：自执行LLM Agent|https://github.com/yoheinakajima/babyagi|
|AutoGPT：自执行LLM Agent|https://github.com/Torantulino/Auto-GPT|
|GPTEngineer：自动工具构建和代码生成|https://github.com/AntonOsika/gpt-engineer|
|Jarvis: 大模型调用小模型框架，给小模型一个未来！|https://github.com/search?q=jarvis|
|LLM-ToolMaker:让LLM自己制造Agent|https://github.com/FMInference/FlexGen|
|Gorilla: LLM调用大量API|https://github.com/ShishirPatil/gorilla|
|wenda:闻达小模型整合搜索用于知识融入|https://github.com/l15y/wenda|
|WorkGPT：类似AutoGPT|https://github.com/team-openpm/workgpt|
|Deep-KE：基于LLM对数据进行智能解析实现知识抽取|https://github.com/zjunlp/DeepKE|

### 开源数据

| 数据类型    | 数据描述    | 数据链接    |
| --- | --- | --- |
|  指令微调   |  self-instruct，GPT3自动生成&过滤得到指令集   |   https://github.com/yizhongw/self-instruct   |
|  指令微调      |    Standford Alpaca：52K text-davinci-003生成的self-instruct指令数据集 |  https://github.com/tatsu-lab/stanford_alpaca   |
|  指令微调      |   GPT4-for-LLM 中文+英文+对比指令| https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM|
|  指令微调      |    GPTTeacher更多样的通用指令，角色扮演和代码指令| https://github.com/teknium1/GPTeacher/tree/main  |
|  指令微调      | 中文翻译Alpaca还有一些其他指令数据集    |    https://github.com/hikariming/alpaca_chinese_dataset https://github.com/carbonz0/alpaca-chinese-dataset|
|指令微调|alpaca指令GPT4生成，和以上几版对比显著质量更高，回复更长|https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM/tree/main|
|  指令微调      |   Guanaco数据：对Alphca指令重写后以不同语言生成总共534K，有对话和非对话类型，还有补充的QA生成样本  | https://huggingface.co/datasets/JosephusCheung/GuanacoDataset    |
|指令微调|OIG中文指令包括翻译alpaca+natural+unnatural，多轮对话，考试，leetcode指令|https://github.com/BAAI-Zlab/COIG|
|指令微调|Vicuna训练使用的样本，用API获取了sharegpt上用户和chatgpt对话历史，部分网友整理到了HF|https://github.com/domeccleston/sharegpt https://huggingface.co/datasets/anon8231489123/ShareGPT_Vicuna_unfiltered/tree/main|
|指令微调|HC3指令数据中英文，包括金融，开放QA，百科，DBQA，医学等包含人工回复|https://huggingface.co/datasets/Hello-SimpleAI/HC3-Chinese/tree/main|
|指令微调|MOSS开源的SFT数据包含使用plugin的对话数据|https://huggingface.co/datasets/Hello-SimpleAI/HC3-Chinese/tree/main|
|指令微调|InstructWild数据：用四处爬取的chatgpt指令作为种子self-instruct扩充生成，中英双语|https://github.com/XueFuzhao/InstructionWild/tree/main/data|
|  指令微调      |  BELLE100万指令数据，参考Alpaca用ChatGPT生成，有数学，多轮对话，校色对话等等   |   https://github.com/LianjiaTech/BELLE  |
|  指令微调      | PromptCLUE多任务提示数据集：模板构建，只包含标准NLP任务     |  https://github.com/CLUEbenchmark/pCLUE   |
|  指令微调      |  TK-Instruct微调用的指令数据集, 全人工标注1600+NLP任务   |   https://instructions.apps.allenai.org/  |
|   指令微调     | T0微调用的指令数据集（P3）    |  https://huggingface.co/datasets/bigscience/P3   |
|  指令微调   | p3衍生的46种多语言数据集（xmtf）    | https://github.com/bigscience-workshop/xmtf    |
|  指令微调      |Unnatural Instruction使用GPT3生成后改写得到240k     |   https://github.com/orhonovich/unnatural-instructions  |
|指令微调|alpaca COT对多个数据源进行了清理并统一格式放到的了HF, 重点是人工整理的COT数据|https://github.com/PhoebusSi/Alpaca-CoT|
|指令微调|人工编写包含23种常见的中文NLP任务的指令数据，中文写作方向|https://github.com/yangjianxin1/Firefly|
|指令微调|Amazon COT指令样本包括各类QA，bigbench，math等|https://github.com/amazon-science/auto-cot|
|指令微调|CSL包含 396,209 篇中文核心期刊论文元信息 （标题、摘要、关键词、学科、门类）可做预训练可构建NLP指令任务|https://github.com/ydli-ai/CSL|
|指令微调|alpaca code 20K代码指令数据|https://github.com/sahil280114/codealpaca#data-release|
|指令微调|GPT4Tools 71K GPT4指令样本|https://github.com/StevenGrove/GPT4Tools|
|指令微调|GPT4指令+角色扮演+代码指令|https://github.com/teknium1/GPTeacher|
|数学|腾讯人工智能实验室发布网上爬取的数学问题APE210k|https://github.com/Chenny0808/ape210k|
|数学|猿辅导 AI Lab开源小学应用题Math23K|https://github.com/SCNU203/Math23k/tree/main|
|数学|grade school math把OpenAI的高中数学题有改造成指令样本有2-8步推理过程|https://huggingface.co/datasets/qwedsacf/grade-school-math-instructions|
|数学|数学问答数据集有推理过程和多项选择|https://huggingface.co/datasets/math_qa/viewer/default/test?row=2|
|数学|AMC竞赛数学题|https://huggingface.co/datasets/competition_math|
|数学|线性代数等纯数学计算题|https://huggingface.co/datasets/math_dataset|
|代码|APPS从不同的开放访问编码网站Codeforces、Kattis 等收集的问题|https://opendatalab.org.cn/APPS|
|代码|Lyra代码由带有嵌入式 SQL 的 Python 代码组成，经过仔细注释的数据库操作程序，配有中文评论和英文评论。|https://opendatalab.org.cn/Lyra|
|代码|Conala来自StackOverflow问题,手动注释3k，英文|https://opendatalab.org.cn/CoNaLa/download|
|代码|code-alpaca ChatGPT生成20K代码指令样本|https://github.com/sahil280114/codealpaca.git|
|对话指令|LAION 策划的开放指令通用数据集中手动选择的组件子集 已开源40M 3万个,100M在路上 |https://github.com/LAION-AI/Open-Instruction-Generalist|
|  对话指令      |Baize基于Chat GPT构建的self-chat数据    |   https://github.com/project-baize/baize-chatbot/tree/main/data   |
|  对话指令      |FaceBook开源BlenderBot训练对话数据~6K     |   https://huggingface.co/datasets/blended_skill_talk   |
|  对话指令      |AllenAI开源38.5万个对话高质量数据集SODA   |   https://realtoxicityprompts.apps.allenai.org/ |
|  对话指令      |InstructDial在单一对话任务类型上进行指令微调   |  https://github.com/prakharguptaz/Instructdial   |
| 对话指令 |Ultra Chat 两个独立的 ChatGPT Turbo API 进行对话，从而生成多轮对话数据|https://github.com/thunlp/UltraChat|
|对话指令|Awesome Open-domain Dialogue Models提供多个开放域对话数据|https://github.com/cingtiye/Awesome-Open-domain-Dialogue-Models#%E4%B8%AD%E6%96%87%E5%BC%80%E6%94%BE%E5%9F%9F%E5%AF%B9%E8%AF%9D%E6%95%B0%E6%8D%AE%E9%9B%86|
|RLFH|北大河狸开源RLHF数据集10K，1M需要申请|https://huggingface.co/datasets/PKU-Alignment/PKU-SafeRLHF-10K|
|  RLHF     |  Anthropic hh-rlhf数据集   |   https://huggingface.co/datasets/Anthropic/hh-rlhf  |
|RLHF|Stack-exchange上问题对应多个答案，每个答案有打分|https://huggingface.co/datasets/HuggingFaceH4/stack-exchange-preferences/tree/main|
|  RLHF     | Facebook Bot Adversarial Dialogues数据集5K   |  https://github.com/facebookresearch/ParlAI  |
|  RLHF     | AllenAI Real Toxicity prompts   |  https://github.com/facebookresearch/ParlAI  |
|RLHF|OpenAssistant Conversations 160K消息，13500人工生成, 英文为主|https://huggingface.co/datasets/OpenAssistant/oasst1|
| 评估集     | BigBench(Beyond the Imitation Game Benchmark)    |  https://github.com/google/BIG-bench   |
|   评估集       |   Complex QA：用于ChatGPT的评测指令集  |    https://github.com/tan92hl/Complex-Question-Answering-Evaluation-of-ChatGPT |
|   评估集      |   Langchain开源评估数据集  |   https://huggingface.co/LangChainDatasets  |
|评估集|2010-2022年全国高考卷的题目|https://github.com/OpenLMLab/GAOKAO-Bench|
|评估集|中文通用大模型综合性评测基准SuperCLUE|https://github.com/CLUEbenchmark/SuperCLUE|
|通用预训练|RedPajama开源的复刻llama的预训练数据集，1.21万亿Token|https://github.com/togethercomputer/RedPajama-Data|
|通用预训练|Cerebras基于RedPajama进行清洗去重后得到的高质量数据集, 6270亿Token|https://huggingface.co/datasets/cerebras/SlimPajama-627B/tree/main/train|
|通用预训练|Pile 22个高质量数据集混合的预训练数据集800G,全量开放下载|https://pile.eleuther.ai/|
|通用预训练|UER整理CLUECorpusSmall+News Commentary中英|https://github.com/dbiir/UER-py/wiki/%E9%A2%84%E8%AE%AD%E7%BB%83%E6%95%B0%E6%8D%AE|
|通用预训练|智源人工智能开源的wudao 200G预训练数据|[https://github.com/BAAI-WuDao/WuDaoMM](https://openi.pcl.ac.cn/BAAI/WuDao-Data)|
|通用预训练|里屋社区发起开源力量收集中文互联网语料集MNBVC目标是对标ChatGPT的40T|https://github.com/esbatmop/MNBVC|
|领域预训练|首个中文科学文献数据集CSL,也有多种NLP任务数据 |https://github.com/ydli-ai/CSL|
|平行语料|news-commentary中英平行语料，用于中英间知识迁移|https://data.statmt.org/news-commentary/v15/training/|
|多源数据集整合|opendatalab整合了预训练阶段的多个数据源|https://opendatalab.org.cn/?industry=9821&source=JUU3JTlGJUE1JUU0JUI5JThF|

## Resources 
### Tools & Tutorial
- [OpenAI Cookbook](https://github.com/openai/openai-cookbook): 提供OpenAI模型使用示例  :star:
- [OpenAI 接口被墙解决办法](https://github.com/riba2534/openai-scf-goproxy): 使用腾讯云搭建代理，亲测非常好用且手残党也可以轻松上手
- [PromptPerfect](https://promptperfect.jinaai.cn/):用魔法打败魔法，输入原始提示词，模型进行定向优化，试用后我有点沉默了，可以定向支持不同使用prompt的模型如Difussion，ChatGPT， Dalle等
- [ClickPrompt](https://www.clickprompt.org/zh-CN/): 为各种prompt加持的工具生成指令包括Difussion，chatgptdeng, 需要OpenAI Key 
- [ChatGPT ShortCut](https://newzone.top/chatgpt/)：提供各式场景下的Prompt范例，范例很全，使用后可以点赞！  :star:
- [Full ChatGPT Prompts + Resources](https://enchanting-trader-463.notion.site/Full-ChatGPT-Prompts-Resources-8aa78bb226b7467ab59b70d2b27042e9): 各种尝尽的prompt范例，和以上场景有所不同
- [learning Prompt](https://learnprompting.org/):  prompt engineering超全教程，和落地应用收藏，包括很多LLM调用Agent的高级场景 :star:
- [The art of asking chatgpt for high quality answers](https://github.com/ORDINAND/The-Art-of-Asking-ChatGPT-for-High-Quality-Answers-A-complete-Guide-to-Prompt-Engineering-Technique): 如何写Prompt指令出书了，链接是中文翻译的版本，比较偏基础使用
- [Prompt-Engineer-Guide]( https://github.com/dair-ai/Prompt-Engineering-Guide): 同learnig prompt类的集成教程，互相引用可还行？！分类索引做的更好些 :star:
- [OpenAI 应用汇总指南](https://www.mojidoc.com/05z7y-dd5pa7hu3zfmhnbngoeztyqcnq-00b): 纯应用类的汇总指南
- [AI 导航](https://www.ainavpro.com/#term-209): 包括但不限于ChatGPT的应用汇总网站，更新很快，发现了一些新大陆
- [AI Alignment Forum](https://www.alignmentforum.org/): RLHF等对齐相关最新论文和观点的讨论论坛
- [Langchain: Chat with your data](https://www.deeplearning.ai/short-courses/langchain-chat-with-your-data/):吴恩达LLM实践课程
- [构筑大语言模型应用：应用开发与架构设计](https://github.com/phodal/aigc): 一本关于 LLM 在真实世界应用的开源电子书

### AIGC playground
- [cognosys](https://www.cognosys.ai/create): 全网最火的web端AutoGPT，不过咋说呢试用了下感觉下巴要笑掉了，不剧透去试试你就知道 ![](https://img.shields.io/badge/Auto-Agent-white)
- [godmode](https://godmode.space/)：需要人为每一步交互的的AutoGPT![](https://img.shields.io/badge/Auto-Agent-white)
- [agentgpt](https://agentgpt.reworkd.ai/): 基础AutoGPT![](https://img.shields.io/badge/Auto-Agent-white)
- [New Bing](https://www.bing.com/)：需要连外网否则会重定向到bing中国，需要申请waitlist ![](https://img.shields.io/badge/AIGC-Search-yellow) :star:
- [Perplexity.ai](https://www.perplexity.ai/): 同样需要科学上网，感觉比Bing做的更好的接入ChatGPT的神奇搜索引擎，在Bing之外还加入了相关推荐和追问 :star:
- [BingGPT](https://github.com/dice2o/BingGPT): NewBing开源桌面客户端，可以将聊天记录导出  ![](https://img.shields.io/badge/AIGC-Search-yellow)
- [DocsGPT](https://github.com/arc53/DocsGPT): 把ChatGPT开放域问答转化成封闭域问答的通用方案，试用垂类领域问答场景,可以试用定制的ChatBot  ![](https://img.shields.io/badge/Tool-Business-red) :star:
- [langchain-ChatGLM](https://github.com/imClumsyPanda/langchain-ChatGLM): 基于ChatGLM的本地知识问答，和上面的DocsGPT相似，不过可以本地部署:star:
- [ChatPDF](https://chat2doc.cn/): 国内的ChatPDF, 上传pdf后，会给出文章的Top5可能问题，然后对话式从文档中进行问答和检索，10s读3万字  ![](https://img.shields.io/badge/Tool-Business-red)
- [ChatDoc](https://chatdoc.com/?viaurl=ainavpro.com):ChatPDF升级版，增加了表格类解析，和完善的索引引用加跳转加对应文章内容高亮，哈哈我准备自己整一个 ![](https://img.shields.io/badge/Tool-Business-red)
- [ChatPaper](https://github.com/kaixindelele/ChatPaper): 根据输入关键词，自动在arxiv上下载最新的论文，并对论文进行摘要总结，可以在huggingface上试用！ ![](https://img.shields.io/badge/Tool-Business-red)
- [OpenRead](https://www.openread.academy/home): 面向论文写作，阅读场景，可以帮助生成文献综述，以及提供和NotionAI相似的智能Markdown用于写作 ![](https://img.shields.io/badge/Tool-Business-red)
- [researchgpt](https://github.com/mukulpatnaik/researchgpt): 和ChatPDF类似，支持arivx论文下载，加载后对话式获取论文重点  ![](https://img.shields.io/badge/Tool-Business-red)
- [BriefGPT](https://briefgpt.xyz/?viaurl=ainavpro.com): 日更Arxiv论文，并对论文进行摘要，关键词抽取，帮助研究者了解最新动态, UI不错哟 ![](https://img.shields.io/badge/Tool-Business-red)
- [ChatGPT-academic](https://github.com/binary-husky/chatgpt_academic): 又是一个基于gradio实现的paper润色，摘要等功能打包的实现 ![](https://img.shields.io/badge/Tool-Business-red)
- [feishu-chatgpt](https://github.com/Leizhenpeng/feishu-chatgpt): 飞书chatgpt，和365copilot相似也是多组件集成, 有点全！  ![](https://img.shields.io/badge/Tool-Business-red)
- [ChatMind](https://www.chatmind.tech/): chatgpt生成思维导图，针对话题的生成还可以，但是针对某本书的就是瞎编了，但是感觉和检索式阅读方式结合效果会出彩~  ![](https://img.shields.io/badge/Tool-Business-red)
- [Shell](): 基于ChatGPT的AI英语聊天工具，口语练习助手
- [AI Topiah](https://www.ai-topia.com/): 聆心智能AI角色聊天，和路飞唠了两句，多少有点中二之魂在燃烧 ![](https://img.shields.io/badge/AIGC-Chatbot-blue)
- [chatbase](https://www.chatbase.co/): 情感角色聊天，还没尝试 ![](https://img.shields.io/badge/AIGC-Chatbot-blue)
- [Vana](https://gptme.vana.com/login): virtual DNA, 通过聊天创建虚拟自己！概念很炫  ![](https://img.shields.io/badge/AIGC-Chatbot-blue)
- [WriteSonic](https://app.writesonic.com/)：AI写作，支持对话和定向创作如广告文案，商品描述, 支持Web检索是亮点，支持中文  ![](https://img.shields.io/badge/AIGC-AI%20wirter%20tools-brightgreen)
- [copy.ai](https://www.copy.ai/): WriteSonic竞品，亮点是像论文引用一样每句话都有对应网站链接，可以一键复制到右边的创作Markdown，超级好用！ ![](https://img.shields.io/badge/AIGC-AI%20wirter%20tools-brightgreen) :star:
- [NotionAI](https://www.notion.so/product?fredir=1)：智能Markdown，适用真相！在创作中用command调用AI辅助润色，扩写，检索内容，给创意idea ![](https://img.shields.io/badge/AIGC-AI%20wirter%20tools-brightgreen)
- [Jasper](https://www.jasper.ai/): 同上，全是竞品哈哈  ![](https://img.shields.io/badge/AIGC-AI%20wirter%20tools-brightgreen)
- [copy.down](https://copyai.cn/): 中文的营销文案生成，只能定向创作，支持关键词到文案的生成  ![](https://img.shields.io/badge/AIGC-AI%20wirter%20tools-brightgreen)
- [ChatExcel](https://chatexcel.com/convert): 指令控制excel计算，对熟悉excel的有些鸡肋，对不熟悉的有点用  ![](https://img.shields.io/badge/Tool-Business-red)
- [ChatPPT](https://github.com/williamfzc/chat-gpt-ppt): 使用ChatGPT进行PPT制作 ![](https://img.shields.io/badge/Tool-Business-red)
- [BibiGPT](https://github.com/JimmyLv/BibiGPT): Bilibli视频内容一键总结，多模态文档  ![](https://img.shields.io/badge/Tool-Business-red)
- Microsoft 365 Copilot：微软Office全面接入GPT4，智能PPT，Excel，Word，暂无链接。其实就是上面开源创意的全家桶套餐 ![](https://img.shields.io/badge/Tool-Business-red)
- Google Workspace: 谷歌推出的搭载各种AI服务的办公场景全覆盖，暂无使用方案。![](https://img.shields.io/badge/Tool-Business-red)
- [Copilot](https://github.com/features/copilot): 要付费哟 ![](https://img.shields.io/badge/AIGC-Coder-blueviolet)
- [Fauxpilot](https://github.com/fauxpilot/fauxpilot): copilot本地开源替代 ![](https://img.shields.io/badge/AIGC-Coder-blueviolet)
- [CodeGex](http://codegeex.cn/zh-CN): 国内替代品，还没试过 ![](https://img.shields.io/badge/AIGC-Coder-blueviolet)
- [Codeium](https://codeium.com/): Copilot替代品，有免费版本支持各种plugin ![](https://img.shields.io/badge/AIGC-Coder-blueviolet)
- [Wolverine](https://github.com/biobootloader/wolverine): 代码自我debug的python脚本 ![](https://img.shields.io/badge/AIGC-Coder-blueviolet)
- [dreamstudio.ai](https://beta.dreamstudio.ai/dream): 开创者，Stable Difussion， 有试用quota ![](https://img.shields.io/badge/AIGC-AI%20Artist-orange)
- [midjourney](https://www.midjourney.com/home/?callbackUrl=%2Fapp%2F): 开创者，艺术风格为主 ![](https://img.shields.io/badge/AIGC-AI%20Artist-orange)
- [Dall.E](https://openai.com/product/dall-e-2): 三巨头这就凑齐了 ![](https://img.shields.io/badge/AIGC-AI%20Artist-orange)
- [ControlNet](https://huggingface.co/spaces/hysts/ControlNet): 为绘画创作加持可控性 ![](https://img.shields.io/badge/AIGC-AI%20Artist-orange)
- [GFPGAN](https://github.com/Nutlope/restorePhotos): 照片修复  ![](https://img.shields.io/badge/AIGC-AI%20Artist-orange)
- [Visual ChatGPT](https://huggingface.co/spaces/microsoft/visual_chatgpt): 微软发布图像ChatGPT，对话方式进行图像生成编辑，问答 ![](https://img.shields.io/badge/AIGC-AI%20Artist-orange) :star:
- [gemo.ai](https://www.genmo.ai/): 多模态聊天机器人，包括文本，图像，视频生成
- [storybird](https://storybird.com/): 根据提示词生成股市绘本，还可以售卖

### Recommend Blog
- [OpenAI ChatGPT Intro](https://openai.com/blog/chatgpt/)
- [OpenAI InstructGPT intro](https://openai.com/blog/instruction-following/)
- AllenAI ChatGPT能力解读：[How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1)  :star:
- Huggingface ChatGPT能力解读：[The techniques behind ChatGPT: RLHF, IFT, CoT, Red teaming, and more](https://huggingface.co/blog/dialog-agents)
- Stephen Wolfram ChatGPT能力解读: [What Is ChatGPT Doing and Why Does It Work?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/)
- [Chatgpt相关解读汇总](https://github.com/chenweiphd/ChatGPT-Hub)
- [麻省理工科技采访OpenAI工程师](https://www.technologyreview.com/2023/03/03/1069311/inside-story-oral-history-how-chatgpt-built-openai/)
- [AGI历史与现状](https://www.jiqizhixin.com/articles/2018-11-15-6?from=timeline)
- [张俊林 通向AGI之路：大型语言模型（LLM）技术精要](https://zhuanlan.zhihu.com/p/597586623)
- [知乎回答 OpenAI 发布 GPT-4，有哪些技术上的优化或突破?](https://www.zhihu.com/question/589639535/answer/2936696161)
- [追赶ChatGPT的难点与平替](https://zhuanlan.zhihu.com/p/609877277)
- [压缩即泛化，泛化即智能](https://zhuanlan.zhihu.com/p/615554635)  :star:
- [陆奇最新演讲实录：我的大模型世界观｜第十四期](https://new.qq.com/rain/a/20230423A08J7400)
- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)  :star:
- [All You Need to Know to Build Your First LLM App](https://towardsdatascience.com/all-you-need-to-know-to-build-your-first-llm-app-eb982c78ffac)  :star:

## Papers
### paper List
- https://github.com/dongguanting/In-Context-Learning_PaperList
- https://github.com/thunlp/PromptPapers
- https://github.com/Timothyxxx/Chain-of-ThoughtsPapers

### 综述
- A Survey of Large Language Models
- Pre-train, Prompt, and Predict: A Systematic Survey of Prompting Methods in Natural Language Processing :star:
- Paradigm Shift in Natural Language Processing
- Pre-Trained Models: Past, Present and Future
- What Language Model Architecture and Pretraining objects work best for zero shot generalization  :star:
- Towards Reasoning in Large Language Models: A Survey
- Reasoning with Language Model Prompting: A Survey :star:
- An Overview on Language Models: Recent Developments and Outlook  :star:

### 大模型能力探究
- LARGER LANGUAGE MODELS DO IN-CONTEXT LEARNING DIFFERENTLY
- Evidence of Meaning in Language Models Trained on Programs
- Sparks of Artificial General Intelligence: Early experiments with GPT-4
- How does in-context learning work? A framework for understanding the differences from traditional supervised learning
- Why can GPT learn in-context? Language Model Secretly Perform Gradient Descent as Meta-Optimizers :star:
- Emerging Ability of Large Language Models :star:
- Rethinking the Role of Demonstrations What Makes incontext learning work? :star:
- Can Explanations Be Useful for Calibrating Black Box Models
- IS CHATGPT A GENERAL-PURPOSE NATURAL LANGUAGE PROCESSING TASK SOLVER?
- Can Large Language Models Infer Causation from Correlation?
- Holistic Evaluation of Language Model
- Harnessing the Power of LLMs in Practice: A Survey on ChatGPT and Beyond
- Theory of Mind May Have Spontaneously Emerged in Large Language Models
- Beyond The Imitation Game: Quantifying And Extrapolating The Capabilities Of Language Models
- On the Robustness of ChatGPT: An Adversarial and Out-of-distribution Perspective

### Tunning Free Prompt
- GPT2: Language Models are Unsupervised Multitask Learners
- GPT3: Language Models are Few-Shot Learners   :star:
- LAMA: Language Models as Knowledge Bases?
- AutoPrompt: Eliciting Knowledge from Language Models

### Fix-Prompt LM Tunning
- T5: Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer
- PET-TC(a): Exploiting Cloze Questions for Few Shot Text Classification and Natural Language Inference  :star:
- PET-TC(b): PETSGLUE It’s Not Just Size That Matters Small Language Models are also few-shot learners
- GenPET: Few-Shot Text Generation with Natural Language Instructions
- LM-BFF: Making Pre-trained Language Models Better Few-shot Learners  :star:
- ADEPT: Improving and Simplifying Pattern Exploiting Training

### Fix-LM Prompt Tunning 
- Prefix-tuning: Optimizing continuous prompts for generation  
- Prompt-tunning: The power of scale for parameter-efficient prompt tuning :star:
- P-tunning: GPT Understands Too :star:
- WARP: Word-level Adversarial ReProgramming

### LM + Prompt Tunning 
- P-tunning v2: Prompt Tuning Can Be Comparable to Fine-tunning Universally Across Scales and Tasks
- PTR: Prompt Tuning with Rules for Text Classification
- PADA: Example-based Prompt Learning for on-the-fly Adaptation to Unseen Domains

### Fix-LM Adapter Tunning
- LORA: LOW-RANK ADAPTATION OF LARGE LANGUAGE MODELS :star:
- LST: Ladder Side-Tuning for Parameter and Memory Efficient Transfer Learning
- Parameter-Efficient Transfer Learning for NLP
- INTRINSIC DIMENSIONALITY EXPLAINS THE EFFECTIVENESS OF LANGUAGE MODEL FINE-TUNING

### 主流LLMS
- GLM-130B: AN OPEN BILINGUAL PRE-TRAINED MODEL
- LLaMA: Open and Efficient Foundation Language Models
- PaLM: Scaling Language Modeling with Pathways
- PaLM 2 Technical Report
- GPT-4 Technical Report
- Backpack Language Models

###  指令微调
- Flan: FINETUNED LANGUAGE MODELS ARE ZERO-SHOT LEARNERS :star:
- Flan-T5: Scaling Instruction-Finetuned Language Models
- Instruct-GPT: Training language models to follow instructions with human feedback :star:
- T0: MULTITASK PROMPTED TRAINING ENABLES ZERO-SHOT TASK GENERALIZATION
- Natural Instructions: Cross-Task Generalization via Natural Language Crowdsourcing Instructions
- Tk-INSTRUCT: SUPER-NATURALINSTRUCTIONS: Generalization via Declarative Instructions on 1600+ NLP Tasks
- Unnatural Instructions: Tuning Language Models with (Almost) No Human Labor
- INSTRUCTEVAL Towards Holistic Evaluation of Instrucion-Tuned Large Language Models
- Mixture-of-Experts Meets Instruction Tuning:A Winning Combination for Large Language Models
### 对话模型
- LaMDA: Language Models for Dialog Applications
- Sparrow: Improving alignment of dialogue agents via targeted human judgements :star:
- BlenderBot 3: a deployed conversational agent that continually learns to responsibly engage
- How NOT To Evaluate Your Dialogue System: An Empirical Study of Unsupervised Evaluation Metrics for Dialogue Response Generation

### Chain of Thought
- 基础&进阶用法
    - [zero-shot-COT] Large Language Models are Zero-Shot Reasoners :star:
    - [few-shot COT] Chain of Thought Prompting Elicits Reasoning in Large Language Models  :star:
    - SELF-CONSISTENCY IMPROVES CHAIN OF THOUGHT REASONING IN LANGUAGE MODELS
    - LEAST-TO-MOST PROMPTING ENABLES COMPLEX REASONING IN LARGE LANGUAGE MODELS :star:
    - Tree of Thoughts: Deliberate Problem Solving with Large Language Models
    - Plan-and-Solve Prompting: Improving Zero-Shot Chain-of-Thought Reasoning by Large Language Models
- 分领域COT
    - Solving Quantitative Reasoning Problems with Language Models
    - COMPLEXITY-BASED PROMPTING FOR MULTI-STEP REASONING
    - Solving math word problems with processand outcome-based feedback
    - CodeRL: Mastering Code Generation through Pretrained Models and Deep Reinforcement Learning
    - T-SciQ: Teaching Multimodal Chain-of-Thought Reasoning via Large Language Model Signals for Science Question Answering
    - LEARNING PERFORMANCE-IMPROVING CODE EDITS
    - Large Language Models are Versatile Decomposers: Decompose Evidence and Questions for Table-based Reasoning 
    - Tab-CoT: Zero-shot Tabular Chain of Thought
- 原理分析
    - Towards Understanding Chain-of-Thought Prompting: An Empirical Study of What Matters  :star:
    - TEXT AND PATTERNS: FOR EFFECTIVE CHAIN OF THOUGHT IT TAKES TWO TO TANGO
    - Towards Revealing the Mystery behind Chain of Thought: a Theoretical Perspective
    - Large Language Models Can Be Easily Distracted by Irrelevant Context
- 小模型COT蒸馏
    - Specializing Smaller Language Models towards Multi-Step Reasoning   :star:
    - Teaching Small Language Models to Reason 
    - Large Language Models are Reasoning Teachers
    - Distilling Reasoning Capabilities into Smaller Language Models
    - The CoT Collection: Improving Zero-shot and Few-shot Learning of Language Models via Chain-of-Thought Fine-Tuning
- others
    - OlaGPT Empowering LLMs With Human-like Problem-Solving abilities
    - Challenging BIG-Bench tasks and whether chain-of-thought can solve them 
    - SHOW YOUR WORK: SCRATCHPADS FOR INTERMEDIATE COMPUTATION WITH LANGUAGE MODELS 
    - STaR: Self-Taught Reasoner Bootstrapping ReasoningWith Reasoning  
    - AUTOMATIC CHAIN OF THOUGHT PROMPTING IN LARGE LANGUAGE MODELS
    - Large Language Models Can Self-Improve
    - Active Prompting with Chain-of-Thought for Large Language Models
    - Large Language Models are Better Reasoners with Self-Verification

### RLHF
- Deepmind
  - Teaching language models to support answers with verified quotes
  - sparrow, Improving alignment of dialogue agents via targetd human judgements :star:
- openai
  - PPO: Proximal Policy Optimization Algorithms :star:
  - Deep Reinforcement Learning for Human Preference
  - Fine-Tuning Language Models from Human Preferences
  - learning to summarize from human feedback
  - InstructGPT: Training language models to follow instructions with human feedback :star:
  - Scaling Laws for Reward Model Over optimization :star:
- Anthropic
  - A General Language Assistant as a Laboratory for Alignmen 
  - Red Teaming Language Models to Reduce Harms Methods,Scaling Behaviors and Lessons Learned
  - Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback  :star:
  - Constitutional AI Harmlessness from AI Feedback :star:
  - Pretraining Language Models with Human Preferences
- AllenAI, RL4LM：IS REINFORCEMENT LEARNING (NOT) FOR NATURAL LANGUAGE PROCESSING BENCHMARKS
- 改良方案 
  - RRHF: Rank Responses to Align Language Models with Human Feedback without tears
  - PRM：Let's verify step by step 
  - Chain of Hindsight Aligns Language Models with Feedback

### Agent: 让模型使用工具
- Prompt方案
  - ReAct: SYNERGIZING REASONING AND ACTING IN LANGUAGE MODELS  :star:
  - Self-ask: MEASURING AND NARROWING THE COMPOSITIONALITY GAP IN LANGUAGE MODELS :star:
  - HuggingGPT: Solving AI Tasks with ChatGPT and its Friends in HuggingFace
  - PAL: Program-aided Language Models
  - ART: Automatic multi-step reasoning and tool-use for large language models
  - Decomposed Prompting A MODULAR APPROACH FOR Solving Complex Tasks
  - Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge-Intensive Multi-Step Questions 
  - Chameleon: Plug-and-Play Compositional Reasoning with Large Language Models
  - ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models
  - Faithful Chain-of-Thought Reasoning
  - ChemCrow Augmenting large language models with chemistry tools
  - Reflexion: Language Agents with Verbal Reinforcement Learning  :star:
  - LLM+P: Empowering Large Language Models with Optimal Planning Proficiency
- 工具微调方案
  - Tool Former: Toolformer: Language Models Can Teach Themselves to Use Tools :star:
  - Tool Learning with Foundation Models
  - Tool Maker： Large Language Models as Tool Maker
  - TALM: Tool Augmented Language Models
  - OpenAGI: When LLM Meets Domain Experts
  - Gorilla： Large Language Model Connected with Massive APIs  :star:
  - WebGPT：Browser-assisted question-answering with human feedback
  - REPLUG: Retrieval-Augmented Black-Box Language Models
- 系统设计
  - MRKL SystemsA modular, neuro-symbolic architecture that combines large language models, external knowledge sources and discrete reasoning
  - WebGLM: Towards An Efficient Web-Enhanced Question Answering System with Human Preferences  :star:
  - TaskMatrix.AI: Completing Tasks by Connecting Foundation Models with Millions of APIs
- 评估
  - Evaluating Verifiability in Generative Search Engines
  - Mind2Web: Towards a Generalist Agent for the Web
  - Auto-GPT for Online Decision Making: Benchmarks and Additional Opinions
  - API-Bank: A Benchmark for Tool-Augmented LLMs
- others
  - Query Rewriting for Retrieval-Augmented Large Language Models
  - RETA-LLM: A Retrieval-Augmented Large Language Model Toolkit
  - Inference with Reference: Lossless Acceleration of Large Language Models
  - Generative Agents: Interactive Simulacra of Human Behavior

### 指令数据生成
- APE: LARGE LANGUAGE MODELS ARE HUMAN-LEVEL PROMPT ENGINEERS  :star:
- SELF-INSTRUCT: Aligning Language Model with Self Generated Instructions :star:
- iPrompt: Explaining Data Patterns in Natural Language via Interpretable Autoprompting  
- Flipped Learning: Guess the Instruction! Flipped Learning Makes Language Models Stronger Zero-Shot Learners
- Fairness-guided Few-shot Prompting for Large Language Models  
- Instruction induction: From few examples to natural language task descriptions.
- Baize An Open-Source Chat Model with Parameter-Efficient Tuning on self-Chat Data
- SELF-QA Unsupervised Knowledge Guided alignment.
- GPT Self-Supervision for a Better Data Annotator

### 领域模型
- BioGPT：Generative Pre-trained Transformer for Biomedical Text Generation and Mining
- Galactia：A Large Language Model for Science
- PubMed GPT: A Domain-specific large language model for biomedical text :star:
- BloombergGPT： A Large Language Model for Finance  
- ChatDoctor：Medical Chat Model Fine-tuned on LLaMA Model using Medical Domain Knowledge
- Med-PaLM：Large Language Models Encode Clinical Knowledge[V1,V2] :star:
- Augmented Large Language Models with Parametric Knowledge Guiding
- XuanYuan 2.0: A Large Chinese Financial Chat Model with Hundreds of Billions Parameters
- ChatLaw Open-Source Legal Large Language Model

### LLM超长文本处理
- Parallel Context Windows for Large Language Models
- Structured Prompting: Scaling In-Context Learning to 1,000 Examples
- [苏剑林, NBCE：使用朴素贝叶斯扩展LLM的Context处理长度](https://spaces.ac.cn/archives/9617) :star:
- Vcc: Scaling Transformers to 128K Tokens or More by Prioritizing Important Tokens
- Unlimiformer: Long-Range Transformers with Unlimited Length Input
- Scaling Transformer to 1M tokens and beyond with RMT
- RECURRENTGPT: Interactive Generation of (Arbitrarily) Long Text 
- TRAIN SHORT, TEST LONG: ATTENTION WITH LINEAR BIASES ENABLES INPUT LENGTH EXTRAPOLATION :star:
- FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness
- Extending Context Window of Large Language Models via Positional Interpolation
- LongNet: Scaling Transformers to 1,000,000,000 Tokens
- [https://kaiokendev.github.io/til#extending-context-to-8k]
- [苏剑林,Transformer升级之路：10、RoPE是一种β进制编码](https://spaces.ac.cn/archives/9675)

### LLM Tunning Practice/Report
- 更少，质量更高的数据带来质变
    - LIMA: Less Is More for Alignment :star:
    - Maybe Only 0.5% Data is Needed: A Preliminary Exploration of Low Training Data Instruction Tuning
    -Textbooks Are All You Need
- 其他
    - BELLE: Exploring the Impact of Instruction Data Scaling on Large Language Models: An Empirical Study on Real-World Use Cases
    - Baize: Baize: An Open-Source Chat Model with Parameter-Efficient Tuning on Self-Chat Data
    - A Comparative Study between Full-Parameter and LoRA-based Fine-Tuning on Chinese Instruction Data for Large LM
    - Exploring ChatGPT’s Ability to Rank Content: A Preliminary Study on Consistency with Human Preferences
    - Towards Better Instruction Following Language Models for Chinese: Investigating the Impact of Training Data and Evaluation

### 提高事实性和解码准确率
- Trusting Your Evidence: Hallucinate Less with Context-aware Decoding  :star:
- SELF-REFINE:ITERATIVE REFINEMENT WITH SELF-FEEDBACK  :star:
- PROMPTING GPT-3 TO BE RELIABLE
- Enhancing Self-Consistency and Performance of Pre-Trained Language Models through Natural Language Inference
- On the Advance of Making Language Models Better Reasoners
- Progressive-Hint Prompting Improves Reasoning in Large Language Models
- ASK ME ANYTHING: A SIMPLE STRATEGY FOR PROMPTING LANGUAGE MODELS  :star:
- Inference-Time Intervention: Eliciting Truthful Answers from a Language Model
- Reflexion: an autonomous agent with dynamic memory and self-reflection

### Other Prompt Engineer 
- Calibrate Before Use: Improving Few-Shot Performance of Language Models
- In-Context Instruction Learning
- LEARNING PERFORMANCE-IMPROVING CODE EDITS
- Boosting Theory-of-Mind Performance in Large Language Models via Prompting
- Generated Knowledge Prompting for Commonsense Reasoning
- RECITATION-AUGMENTED LANGUAGE MODELS

### Multimodal
- InstructBLIP: Towards General-purpose Vision-Language Models with Instruction Tuning
- Visual ChatGPT: Talking, Drawing and Editing with Visual Foundation Models
- PaLM-E: An Embodied Multimodal Language Model


### Others
- Learnware: Small Models Do Big
- The economic potential of generative AI
- A PhD Student’s Perspective on Research in NLP in the Era of Very Large Language Models
