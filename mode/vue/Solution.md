端框架的存在是为了解决什么问题？
在众多的框架之中，Vue独具魅力之处何在？
为什么说其背后的核心思想是渐进式？
Vue究竟火到什么程度？
最近发布的Vue2.0又做了哪些改进呢？
Vue和Weex又是怎样的一种合作？

# 为什么要有框架

1. 框架的存在是为了帮助我们应对复杂度
前端框架特别多，那么为什么要有框架呢？我个人的看法是，框架的存在是为了帮助我们应对复杂度。当我们需要解决一些前端上工程问题的时候，这些问题会有不同的复杂度。如果你用太简陋的工具应对非常复杂的需求，就会极大地影响你的生产力。所以，框架本身是帮我们把一些重复的并且已经受过验证的模式，抽象到一个已经帮你设计好的API封装当中，帮助我们去应对这些复杂的问题。

2. 框架自身也有复杂度
但是，框架本身也会带来复杂度。相信大家在调研各种框架或学习各种框架时，会遇到学习曲线问题——有些框架会让人一时不知如何上手。

这里就抽象出一个问题，就是要做的应用的复杂度与所使用的框架的复杂度的对比。 进一步说，是所要解决的问题的内在复杂度，与所使用的工具的复杂度进行对比。

3. 工具复杂度是为了处理内在复杂度所做的投资
工具的复杂度是可以理解为是我们为了处理问题内在复杂度所做的投资。为什么叫投资？那是因为如果投的太少，就起不到规模的效应，不会有合理的回报。这就像创业公司拿风投，投多少是很重要的问题。如果要解决的问题本身是非常复杂的，那么你用一个过于简陋的工具应付它，就会遇到工具太弱而使得生产力受影响的问题。
反之，是如果所要解决的问题并不复杂，但你却用了很复杂的框架，那么就相当于杀鸡用牛刀，会遇到工具复杂度所带来的副作用，不仅会失去工具本身所带来优势，还会增加各种问题，例如培训成本、上手成本，以及实际开发效率等。


4. Pick the right tool for the job
“Pick the right tool for the job”——在国外，跟开发者讨论一些框架选型问题时，大家都会说这句话——一切都要看场景。因为，前端开发原生开发或者桌面开发模式相比，有自己的独特之处，它跟其实并不那么固定。在Web上面，应用可以有非常多的形态，不同形态的Web应用可能有完全不同程度的复杂度。这也是为什么我要谈工具复杂度和所要做的应用复杂度的问题。

5. 怎么看前端框架的复杂度

前的前端开发已经越来越工程化，而我们需要解决的实际问题也是不同的。我们就下图进行分析。

声明式渲染=》组件系统=》客户端路由=》大规模状态管理=》构建工具

我们可能在任何情况下都需要声明式的渲染功能，并希望尽可能避免手动操作，或者说是可变的命令式操作，希望尽可能地让DOM的更新操作是自动的，状态变化的时候它就应该自动更新到正确的状态；我们需要组件系统，将一个大型的界面切分成一个一个更小的可控单元；客户端路由——这是针对单页应用而言，不做就不需要，如果需要做单页应用，那么就需要有一个URL对应到一个应用的状态，就需要有路由解决方案；大规模的状态管理——当应用简单的时候，可能一个很基础的状态和界面映射可以解决问题，但是当应用变得很大，涉及多人协作的时候，就会涉及多个组件之间的共享、多个组件需要去改动同一份状态，以及如何使得这样大规模应用依然能够高效运行，这就涉及大规模状态管理的问题，当然也涉及到可维护性，还有构建工具。现在，如果放眼前端的未来，当HTTP2普及后，可能会带来构建工具的一次革命。但就目前而言，尤其是在中国的网络环境下，打包和工程构建依然是非常重要且不可避免的一个环节。 

# 主流框架分析

我们看一下现有的一些主流框架从少到多所解决的问题。这个多少并不是来评价框架的好坏，而是从设计的角度出发看它涵盖多少内容。

纯模板引擎：最少的就是纯模板引擎，只管状态到界面的映射。
React和Vue：其实这两者都是非常专注的只做状态到界面映射，以及组件。
Backbone：它会给你多一些架构上指导，比如它会让你分层。
Angular：它做的事情就更多，它有自己的路由，这些都会包含在里面。
Ember：相比Angular，Ember做得就更加彻底，Ember信奉的是约定优于配置，它会将一切都帮你设计好打包好，你就开箱用就可以了。
Meteor：Meteor只是一个极端，它是从前到后全都包含，从前端到数据层到数据库，全都帮你打包好。

通过简单的分析，我们可以感受到，做得少的框架不一定就不如做得多的框架，这体现出一种取舍。也就是说，做得少的框架可以给你更多的灵活性，但你需要做更多的选择；做得多的框架有更强的侵入性，学习成本更高，灵活性更低。一旦选择了一个侵入性强的框架，那么一些小的部分你就没有机会去切换成其他你更想用的方案。

所以，React和Vue有一个共同特点，它们都有各自的配套工具，核心虽然只解决一个很小的问题，但它们有生态圈及配套的可选工具，当你把他们一个一个加进来的时候，就可以组合成非常强大的栈，就可以涵盖其他的这些更完整的框架所涵盖的问题。



这样的一个配置方案，使得在你构建技术栈的时候有可弹性伸缩的工具复杂度：当所要解决的问题内在复杂度很低的时候，可以只用核心的这些很简单的功能；当需要做一个更复杂的应用时，再增添相应的工具。例如做一个单页应用的时候才需要用路由；做一个相当庞大的应用，涉及到多组件状态共享以及多个开发者共同协作时，才可能需要大规模状态管理方案。

一个纯粹的复杂的单页应用，和只是在后端渲染的静态页面上嵌入交互内容所需要选择的工程栈其实是有相当大区别的。这就是为什么我觉得，核心+生态的栈会是一个在整体选型更为灵活的栈。

React和Vue都选择这个模式。Facebook团队只是专注做React本身，但React社区非常活跃，贡献了大量的第三方解决方案。不可否认，React社区是当前最活跃的社区，很多优秀的想法和思路，包括状态管理方案最早都是从React社区萌发出来。但是社区的这种活跃也带来一定程度的副作用，那就是时代变化太快，三天出一个新版本，同一个问题曾经存在几十种不同的解决方案。这就使得我们在去搭建自己的栈时，需要花很多的时间去鉴别所选择的部件。同时，由于整个生态圈的这些库并不是由一个统一的团队去规划和设计的，所以很难考虑到不同的库之间的协作，这就会导致磨合问题。

同时，这也使得很多开发者抱怨有一个“JavaScript Fatigue”，说JS生态圈东西太多了，为了跟上潮流，需要不停学习最新的东西，觉得很累。当然，有很多人觉得这是生态圈繁荣的表现，但它确实使得大家面临了选择困难症的问题。

Dan Abramov 是之前React社区非常活跃的开发者，已经加入了React团队。有一天他在推特上说，极度的模块化使得他非常难去构建一个统一的体验。这句话指的就是，React生态圈整个栈的每一个部分来自不同开发者，想全部整合到一起的时就有很多零碎的问题。这是他刚开始做React现在的官方的CLI的时候发出的感慨，他在试图整合社区的各种东西放到一个架子里面，于是遇到了很多这样的问题。我这里完全没有否认React生态圈繁荣的意思，我只是觉得可以有另外一种选择，那就是我们可以做一个渐进式框架，这就是Vue选择的方向。


# Vue.js的定位

我在做Vue的过程中也在不停地思考它的定位，现在，我觉得它与其他框架的区别就是渐进式的想法，也就是“Progressive”——这个词在英文中定义是渐进，一步一步，不是说你必须一竿子把所有的东西都用上。

## Vue的设计


Vue从设计角度来讲，虽然能够涵盖这张图上所有的东西，但是你并不需要一上手就把所有东西全用上，因为没有必要。无论从学习角度，还是实际情况，这都是可选的。声明式渲染和组建系统是Vue的核心库所包含内容，而客户端路由、状态管理、构建工具都有专门解决方案。这些解决方案相互独立，你可以在核心的基础上任意选用其他的部件，不一定要全部整合在一起。