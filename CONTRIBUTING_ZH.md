# 贡献到 eunomia-bpd

eunomia-bpd 团队鼓励社区反馈和贡献。
感谢您对改进 eunomia-bpd 的兴趣！有几种方式可以参与其中。

如果您希望为项目做出贡献，请：

* 查看 [可用的问题模板](https://github.com/eunomia-bpf/bpftime/issues/new/choose)
并查看 [好的初学问题示例](https://github.com/eunomia-bpf/bpftime/contribute)
（或[点击这里](https://github.com/eunomia-bpf/bpftime/labels/good%20first%20issue)）。

* 浏览需要帮助的 [问题列表](https://github.com/eunomia-bpf/bpftime/labels/help%20wanted)。

## 报告问题和建议新功能

如果您发现项目无法正常工作，请使用 [Bug 报告模板](https://github.com/eunomia-bpf/bpftime/issues/new?assignees=&labels=bug&template=bug_report.md&title=[BUG]) 提交报告。
如果提供的模板不符合您的需求，请随意创建 [自定义问题报告](https://github.com/eunomia-bpf/bpftime/issues/new?assignees=&labels=&projects=&template=custom.md&title=)，但请相应地标记它。

我们很乐意听取您对如何进一步改进 eunomia-bpd 的想法，确保它符合您的需求。查看 [问题](https://github.com/eunomia-bpf/bpftime/issues) 看看是否有其他人提交了类似的反馈。您可以通过点赞现有反馈（使用点赞反应/评论）或[提交新建议](https://github.com/eunomia-bpf/bpftime/labels/feature)来参与讨论。

我们在决定下一步工作内容时始终关注被点赞的项目 [Issues](https://github.com/eunomia-bpf/bpftime/issues)。我们会阅读评论，期待听到您的意见。

## 找到您可以帮助解决的问题

寻找可以处理的问题？
标记为 [好的初学问题](https://github.com/eunomia-bpf/bpftime/labels/good%20first%20issue) 是一个很好的开始。

您还可以检查 [帮助请求](https://github.com/eunomia-bpf/bpftime/labels/help%20wanted) 标签，找到其他可以帮助的问题。如果您有兴趣解决问题，请留下评论以告知大家，并避免其他人重复努力。

## 我们接受的贡献

我们非常感谢任何帮助我们改进最终产品的贡献，尤其是您能够创建的任何修复错误和直接改进的高优先级问题。一些一般性指导方针：

### 可行性

* **DO** 为每个问题创建一个拉取请求，并确保问题在拉取请求中有链接。您可以按照拉取请求模板进行操作。

* **DO** 遵循我们的 [编码和风格](#style-guidelines) 指南，并尽可能保持代码更改尽可能小。

* **DO** 在可能的情况下包含相应的测试。

* **DO** 在提交 PR 之前检查代码库中其他部分是否存在相同问题的其他出现。

* **DO** 在拉取请求中链接您正在解决的问题。

* **DO** 为您的拉取请求编写良好的描述。详细的信息更好。描述*为什么*正在进行更改和*为什么*选择特定解决方案。描述您执行的任何手动测试以验证您的更改。

### 不可行性

* **DO NOT** 将多个更改合并到一个 PR 中，除非它们具有相同的根本原因。

> 为经过批准的问题提交拉取请求并不保证会被批准。
> 更改必须符合我们的高代码质量、架构和性能标准。

## 更改代码

### 准备开发环境

要了解如何构建代码并运行测试，请按照 [README](README.md) 中的说明操作。

### 风格指南

该项目中的代码使用几种不同的编码样式，具体取决于代码的年龄和历史。请尽可能匹配周围代码的样式。在新组件中，请优先使用 [C++ 核心指南](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) 中描述的模式。

### 测试

您的更改应包括尽可能验证新功能的测试。代码应该结构化，以便可以独立于 UI 进行单元测试。在无法进行自动化测试的情况下，应使用手动测试用例。

### Git 工作流程

在项目的 Git 工作流程中，核心原则是主分支应始终处于可发布的健康状态。主分支上的每个提交都应该可以在推送时部署。为了确保这一点，**不应** 直接在主分支上进行拉取请求。每个更改应该在开发分支（命名为开发的变体，例如 dev）或单独的分支中进行。

如果您的更改比较复杂，请在提交拉取请求之前清理分支历史记录。您可以使用 [git rebase](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) 将您的更改分组为少量提交，我们可以逐个审查。

完成拉取请求后，我们通常会将您的更改合并为一个提交。在确认更改按预期工作后，分支*可能*会被删除，以防止分支污染。如果您的拉取请求需要作为单独的提交合并，请告知我们。

### 持续集成

对于此项目，CI 由 [GitHub Actions](https://github.com/features/actions) 提供，工作流程位于 [.github/workflows 文件夹](.github/workflows) 中。工作流程会自动在每个提交上运行，除非特别指定跳过该提交。

要在特定提交上跳过 CI 运行，请在提交消息中包含 [skip ci] 或 [ci skip]。

bash
# 不触发 CI 工作流程的提交消息示例
git commit -m "我的正常提交消息 [skip ci]"
# 或
git commit -m "我的正常提交消息 [ci skip]"

## 审查过程

提交拉取请求后，团队成员将审查您的代码。我们会将请求分配给适当的审阅人员（如果适用）。社区的任何成员都可以参与审查，但项目团队至少会有一名成员最终批准请求。

通常，需要多次迭代或讨论以响应审阅人员的反馈。尝试查看[过去的拉取请求](https://github.com/eunomia-bpf/bpftime/pulls?q=is%3Apr+is%3Aclosed)，了解体验可能会是什么样子。

## 贡献者许可协议

在我们能够审查和接受您的拉取请求之前，您需要签署一份贡献者许可协议（CLA）。CLA 确保社区可以自由使用您的贡献。签署 CLA 是一个手动过程，您需要为每个提交的拉取请求进行操作。这是通过检查拉取请求准备性检查表中的框来完成的。

### 重要提示

***检查上述框表示您同意为整个社区提供您的更改和/或代码免费使用，并且受到更改的约束！***

在您准备创建拉取请求之前，无需签署 CLA。当您创建拉取请求时，它将由团队成员审查。

