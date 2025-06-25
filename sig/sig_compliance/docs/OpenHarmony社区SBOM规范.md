# OpenHarmony社区SBOM规范与指导

## 目的

软件物料清单（Software Bill of Materials）后续缩写为SBOM，其本身在开源治理领域属于新兴的概念与规范，大量新的关于SBOM的行业规范指导与优秀实践正在不断涌现，为了帮助社区开发者及社区上下游组织，更好的理解、导入、消费OpenHarmony社区的SBOM，本文基于行业的各类各种规则规范和优秀实践结合OpenHarmony社区要求，对OpenHarmony社区在SBOM的定义、生成、消费、与上下游进行交换等主要活动进行规范和指导，以帮助社区更好的理解SBOM的术语、分类、能力等级、使用场景，并达成一致，同时满足在安全、合规、第三方开源软件管理等对社区SBOM的需求。

**特别说明：** 由于SBOM的规范和实践在国内和国外都发展的非常快速，本文中所做出的规定和指导，需要随新的标准规范发生变化，尽管本文会尽可能的与最新标准规范保持一致， 但若本规范中有与业界标准规范冲突之处，请以业界规范、标准为准，并欢迎反馈至本规范。

## 范围

本指导适用于OpenHarmony社区的发布版本（含正式版本、LTS版本、beta版本）

## 本文的改进和修订说明

1. 本文档由合规SIG主导起草和维护。最新版本可以在 [这里](OpenHarmony SBOM规范与指导.md)找到。
2. 任何对于本文中涉及的规则的增加，修改，删除都必须可追溯 。
3. 最终规则经过社区充分的讨论后，由PMC评审定稿。

## 术语和缩略语

|  术语  | 说明  |
| :------------ | :------------ |
| SBOM| 对源代码或二进制基于静态程序分析等技术进行规则检查，用于保障代码的规范、安全、合规 |
| 开源义务履行| 依据所使用开源软件中的开源许可证中所规定的条款要求，对条款规则中要求的义务项进行履行 |
| NOTICE| 即开源软件使用声明，是常见的许可证中规定的义务项所对应的交付件 |


## SBOM的定义
### SBOM的定义
什么是 SBOM
SBOM 是软件物料清单（Software Bill of Materials）的缩写。它是一份详细记录软件中使用的所有组件、库和依赖项的清单。包括开源软件组件、第三方库等。每个元素在 SBOM 中会有详细的信息，如名称、版本号、许可证信息、依赖关系等。
2021年7月12日美国在关于改善国家网络安全的行政命令（EO 14028第10节）中将SBOM定义为“包含构建软件中使用的各种组件的详细信息和供应链关系的正式记录”。

### SBOM的用途
SBOM 的目的是增加软件供应链的可见性和透明度，并提供更好的风险管理和安全性。它可以帮助软件开发者、供应商和用户了解其软件中使用的组件和依赖项，以便更好地管理潜在的漏洞、安全风险和合规性问题。通过 SBOM 用户可以识别和跟踪软件中存在的任何潜在漏洞或已知的安全问题，并及时采取相应的补救措施。
SBOM 还可以用于软件审计、合规性要求和法规遵从性等方面。一些行业标准和法规（如软件供应链安全框架（SSCF）和欧盟网络和信息安全指令（NIS指令））已经要求软件供应商提供 SBOM，以提高软件供应链的安全性和可信度。

### SBOM的分类

SBOM可在不同的软件声明周期内进行生成，因此SBOM也会存在因为生成的时间节点不同，而产生不同类型的SBOM，不同类型的SBOM各自尤其优势和限制，通常业界将其划分为以下几种类型

| SBOM分类| 定义 | 数据描述 | 优势 | 限制 |
| ------------- | ---- | -------- | ---- | ---- |
| Design SBOM   | 早期阶段，成分可能不全，描述新软件 | 来自设计规范和一些初始概念  | 在引入前显示不兼容的软件 | 相比其他类型的SBOM，信息不够详细 |
| Source SBOM   | 直接来源于开发环境中的源文件、以及用于构建的依赖信息 | 主要通过SCA之类工具进行分析，人工确认     |不兴国构建就可以提供可视信息，可以促进从源头开始避免引入致命/严重漏洞，提供依赖关系树，依赖+ 层次关系 |依赖于变成语言生态系统，可能不会包含运行态，插件、或者动态依赖，如系统库文等依赖其他类型来确保成分+依赖的完整性 |
| Build SBOM    | 作为构建软件过程的一部分生成SBOM，已从源文件、依赖项、构建组件、构建过程临时数据和其他SBOM等数据创建可发布的制品| 典型场景是作为构建过程一部分，可能包含产生最终阀部件的构建中间+ 源SBOM     | 随构建CI/CD流程产生，提升SBOM正确性保障，提供更多可见性，不仅仅时源代码。可以随产品发布件同一个构建流程进行签名，提升信任 |高度依赖构建执行的实际华景，对于间接依赖或运行依赖，在构建中铺货会比较困难。 |
| Analyzed SBOM | 构建后，通过第三方工具分析artifacts（可执行文件、包、容器）得到。类似分析方法通常需要探索性算法，一定意义上，通常成为第三方SBOM，Analyzed SBOM可以在一定程度上与提供方的SBOM验证正确性| 通常采用第三方工具对artifacts进行扫描/分析  | 不需要访问构建过程，可以作为其他类型SBOM数据验证 |如果工具无法精确分解或识别软件组件，可能容易出现遗漏、错误等。 |
| Deployed SBOM | SBOM提供系统上存在的软件清单。 这可能时其他SBOM的集合，它结合了配置选型的分析和部署环境中的执行行为检查 | 通常通过记录已安全在系统上的软件的SBOM和配置信息生成     | 显示系统上安装的软件，包括用于运行应用程序的其他配置和系统软件 | 可能会要修改安装/部署过程，可能无法准确描述运行环境 |
| Runtime SBOM  | 通过检测运行软件的系统生成的SBOM，已仅捕获系统中存在的组件，以及外部标注或动态加载的组件。在某些情况下，这也可以成为“仪器化”或“动态”SBOM     | 通常由与系统交互的工具生成，以记录运行环境中存在的或已执行的artifacts  | 提升系统运行状况可见性，包括动态加载和外部链接，包括哪些被激活，哪些被使用的状态  | 需要在运行时分析系统，可能需要额外开销。有些详细信息可能需要系统运行一段时间后才能获得。  |

OpenHarmony社区当前核心关注**两类SBOM的生成与使用**：Source SBOM（基于全量源码）和Build SBOM（基于设备形态中使用的部件）

## OpenHarmony社区SBOM最小集规范
参照业界对于SBOM最小集的要求，结合OpenHarmony社区中安全治理、开源软件管理、开源合规治理诉求特对OpenHarmony社区SBOM进行以下三方面的规范

1. **SBOM各组件最小数据集** ：即SBOM清单中每个组件中至少（*必须*）需要包含的关键信息
2. **SBOM生成、消费流程及管理规范** ：即对于SBOM的生成、发布、消费、申请、访问、勘误等流程的规范
3. **SBOM自动化支持格式**：即SBOM清单在表达关键信息时需要遵从的格式、关键字、嵌套表达方式要求，此格式在SBOM生成和SBOM消费环节都需要使用，并且要做到*机器可读*。

### OpenHarmony社区安全治理、开源合规治理、开源软件管理诉求汇总
1. 安全治理：开源软件成分的准确全面
2. 开源合规：许可证信息准确
3. 开源管理：软件生命周期满足要求，状态与部件实时同步，二进制管理

### OpenHarmony SBOM 各组件最小数据集规范
组件最小数据集是指作为每个组件必须包含的数据信息的集合，通过本数据集，应可以充分完整的追溯到该组件中成分的原始信息，再进一步基于这些最小集信息，可以根据不同的场景诉求，生成对应的满足安全治理、合规治理等SBOM信息。

| 最小集数据字段（英文）         | 数据字段（中文  | 描述                                    |
| ------------------------- | ------------ | ----------------------------------- |
| Supplier Name             | 供应商名称   | 创建，定义，识别此组件的组织或单位名称       |
| Component Name            | 组件名      | 由原始供应商定义的组件名称Text             |
| Version of the Component  | 组件版本号   | 标识符，用于供应商标识与上一版本之前的变更    |
| Other Unique Identifiers  | 其他标识符   | 其他可以用于标识一个组件的标识符            |
| Dependency Relationship   | 依赖关系     | 表示依赖关系，如软件Y包含一个上游组件X      |
| Author of SBOM Data       | SBOM数据作者 | 创建此组件SBOM数据清单的组织或单位名称      |
| Timestamp                 | 时间戳       | SBOM数据清单生成的日期与时间              |

| 最小集数据字段（英文）         | 数据字段（中文  | 描述                                |
| ------------------------- | ------------ | ----------------------------------- |
| Hash of the Componet      | 组件哈希值     | 组件的哈希值，确保组件的完整性           |
| Lifecycle Phase           | SBOM生成阶段  | 不同阶段生成的SBOM不同，明确具体的生成时间点|
| Other Component Relationships| 其他类型组件关系 | 如衍生关系和后代关系                |
| License Information       | 许可证信息       | 许可证信息，用于识别合规风险          |

### SBOM生成、消费流程及管理规范
SBOM不仅仅是一组清单数据，更重要的是将SBOM融于整个软件开发生命周期之中，按照一定策略进行治理和上下游交换的能力。

#### SBOM发布频率
OpenHarmony SBOM发布节奏跟随OpenHarmony社区版本发布节奏，其中Release版本及LTS版本会发布正式的SBOM，并持续对Release及LTS版本的SBOM信息进行维护和更新。  而beta版本仅对内部做SBOM的生成，主要用于验证SBOM机制的准确性和阶段性对beta版本数据进行校准，不进行后期的维护。

#### SBOM依赖软件深度
根据业界的实践，OpenHarmony SBOM至少需要包含全部主软件（顶层依赖），并应尽可能的提供更多信息，以便使用者可以根据主软件信息自行识别其传递依赖。对于下层依赖，OpenHarmony社区也应按照社区能力，持续加强支持深度，后续支持用户根据自身
需求选择SBOM中依赖软件的深度。

#### SBOM中已知的未知
业界中尽快有大量优秀实践，但都很难真正遍历全部下层依赖和成分，SBOM中必须对已知的没有进行深度依赖分析的情况，表示出known unknown（如spdx中使用NOASSERTION），用于区别出经过分析后确实没有下层依赖的情况，向SBOM使用者提示，对应的组件有可能含有下层依赖。

#### OpenHarmony SBOM 分发
OpenHarmony SBOM 当OpenHarmony软件版本发布后，在OpenHarmony数字化协作平台按版本进行归档，具有SBOM查看权限者，可以通过[此处](http://ci.openharmony.cn/workbench/opensource/thirdpartysource/bomlist/list)进行查阅。
OpenHarmony社区自身的服务可以通过基础设施的API接口获取相关数据进行进一步的治理与应用
#### OpenHarmony SBOM 访问控制
由于SBOM作为核心数据，本身的全量导出应有一定的访问控制，当前SBOM的访问权限定义为PMC成员 + 合规SIG Leader + 安全SIG Leader，但关于SBOM数据的应用结果，应向社区开放。
#### OpenHarmony SBOM 勘错
由于大型开源软件的复杂性，SBOM很难完全准确，社区通过[issue](https://gitee.com/openharmony/community/issues)来接收SBOM的错误，社区在确认后，即会定期更新SBOM的内容及新版本

### OpenHarmony SBOM自动化支持格式

当前业界具备共识的SBOM格式，主要有以下三种：
- Software Package Data eXchange([SPDX](https://spdx.dev/))
- [CycloneDX](https://cyclonedx.org/)
- Software Identification(SWID)tags

OpenHarmony社区在SBOM格式上当前重点支持SPDX和CycloneDX两种格式

#### SPDX格式的表达方式规范
SPDX 2.2 json格式

文件后缀要求： ·*.spdx.json

根据SPDX格式要求

![图片](https://spdx.github.io/spdx-spec/v2.2.2/img/spdx-2.2.2-document.png)

| NTIA SBOM Minimum Field | Satisfying SPDX field |
| --- | --- |
| Author Name | (6.8) Creator |
| Supplier Name | (7.5) Package Supplier |
| Component Name | (7.1) Package Name |
| Version String | (7.3) Package Version |
| Component Hash | (7.10) Package Checksum |
| Unique Identifier | (7.2) Package SPDX Identifier  <br>(6.5) SPDX Document Namespace |
| Relationship | (11.1) Relationship:`CONTAINS`,`DESCRIBES`  <br>The document must`DESCRIBES`at least one package. |
| Timestamp | (6.9) Created |

##### 组件表示方法
OpenHarmony SBOM SPDX格式规范
##### SPDX document creation information section
```
- "spdxVersion" : "SPDX-2.2",  当前固定SPDX-2.2
- "dataLicense" : "CC0-1.0",   当前固定CC0-1.0
- "SPDXID" : "SPDXRef-ability_lite"， ID命名规则。
- "name": "ability_lite-OpenHarmony_4.0" ， 为DocumentName文档名，命名规则 XXX-YYY, 其中XXX为组件名，YYY为该组件对应版本号
- "documentNamespace" : null， 当前为null，后续sbom资源归档至网站后，使用此格式进行填充"http://[CreatorWebsite]/[pathToSpdx]/[DocumentName]-[UUID]"
-  "creationInfo" : {
    "created" : "2010-01-29T18:30:22Z",   SBOM初始创建时间 YYYY-MM-DDThh:mm:ssZ   **对应NTIA中Timestamp**
    "creators" : [ "Organization: OpenHarmony" ]   SBOM创建的实体组织名称，**对应NTIA中Author Name**，OpenHarmony SBOM 缺省填写OpenHarmony
  }
```

##### SPDXID 命名规则  
- SBOM 清单文档 : SPDXRef-DOCUMENT
- 产品大包：  SPDXRef-PRODUCT
- 源码仓： SPDXRef-SOURCE-源码仓名
- 第三方上游软件： SPDXRef-UPSTREAM-软件名
- 文件/二进制： SPDXRef-路径，其中/改为-
- 软件包：SPDXRef-Package-包名
- 部件：SPDXRef-Componet-部件名


##### Package information section
```
  "packages" : [ {
    "SPDXID" : "SPDXRef-SOURCE-ability-ability_lite",    **SPDXID 命名规则** 。
    "filesAnalyzed" : "true",     **相较SPDX额外作为必选**， 基于源码的SBOM，此字段为true，即可以基于此组件进行文件级分析，基于构建制品的SBOM，需按场景使用，若有两组件静态链接的情况，A静态链接B，A把B包含了，B组件需要写package，但在此字段需要填false，并在relationship中标识静态链接关系。
    "name" : "ability_base",                 组件全名，要求为**原始组件全名**，若为第三方软件，则写上游软件名， **对应NTIA中的Component Name**
    "supplier" : "Organization: OpenHarmony",     **相较SPDX额外作为必选**， **对应NTIA中的Supplier Name**，实际分发者，不一定与原始分发者一致，不能只是分发网站，要对应组织名，当前OpenHarmony的源，均为OpenHarmony分发，第三方软件亦是由OpenHarmony仓库托管分发
    "versionInfo" : "OpenHarmony-4.0-Release"  **相较SPDX额外作为必选**，**对应NTIA中的Version of the Component**组件版本信息，用于表示版本变化，
    "PackageFileName"："./myrootdir/mysubdir1 or glibc-2.11.1.tar.gz"  **相较SPDX额外作为必选**， 源码使用下载后的源码路径，软件包使用包名
    "originator" : "Organization: ExampleCodeInspect (contact@example.com)",  **相较SPDX额外作为必选**，原始供应商，自研组件填写OpenHarmony,第三方组件填写上游原始供应商
    "downloadLocation" : "http://ftp.gnu.org/gnu/glibc/glibc-ports-2.15.tar.gz",   软件下载地址，自研组件 可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeExcludedFiles" : [ "./package.spdx" ],
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 基于构建制品的SBOM必填此字段，基于源码的SBOM，同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],
    "homepage" : "http://ftp.gnu.org/gnu/glibc",   **相较SPDX额外作为必选**，三方组件填上游社区网址，自研组件统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "(LGPL-2.0-only OR LicenseRef-3)",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseInfoFromFiles" : [ "GPL-2.0-only", "LicenseRef-2", "LicenseRef-1" ],   **合规必选****相较SPDX额外作为必选**，作为推论许可证中的参考依据，应包含组件中全量许可证信息，在此不做许可证间关系说明，由工具扫描文件级许可证，必须为SPDX License Expression
    "licenseDeclared" : "(LGPL-2.0-only AND LicenseRef-3)",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "licenseComments" : "The license for this project changed with the release of version x.y.  The version of the project included here post-dates the license change.",   **合规必选**
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  可多行
    "description" : "The GNU C Library defines functions that are specified by the ISO C standard.", **开源管理必选**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/ability_ability_base@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       },   {
      "referenceCategory" : "SECURITY",
      "referenceLocator" : "cpe:2.3:a:pivotal_software:spring_framework:4.1.0:*:*:*:*:*:*:*",
      "referenceType" : "cpe23Type"
      }],
    "primaryPackagePurpose" : "FRAMEWORK", **相较SPDX额外作为必选** **开源管理必选**, 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间
```

##### File information section
根据SBOM的不同深度等级，可以补充每个package下的文件级SBOM信息，当前优先完成package级的SBOM定义，文件级SBOM在第二版进行支持和定义
```
{
    "filename":"/system/lib/libdXXX.so"      **构建SBOM额外作为必选**
    "SPDXID":"SPDXRef-system-lib-libdXXX.so"
    "checksums": [
        {
			"algorithm":"SHA1",
            "checksumValue": "279XXXXXXXXXXXXXXXXXXXX"
        }
    ]
}
```

##### Snippet information section
由于OpenHarmony社区中禁止对第三方开源代码片段引用，因此SBOM中不在单独定义Snippet的使用格式与规范

 
##### Other licensing information detected section
```
   "hasExtractedLicensingInfos" : [ {         **开源合规必选**  非SPDX标准License， 需要补充以下字段
        "licenseId" : "LicenseRef-1",
        "extractedText" : "/*\n * (c) Copyright 2000, 2001, 2002, 2003, 2004, 2005, 2006, 2007, 2008, 2009 Hewlett-Packard Development Company, LP\n * All rights reserved.\n *\n * Redistribution and use in source and binary forms, with or without\n * modification, are permitted provided that the following conditions\n * are met:\n * 1. Redistributions of source code must retain the above copyright\n *    notice, this list of conditions and the following disclaimer.\n * 2. Redistributions in binary form must reproduce the above copyright\n *    notice, this list of conditions and the following disclaimer in the\n *    documentation and/or other materials provided with the distribution.\n * 3. The name of the author may not be used to endorse or promote products\n *    derived from this software without specific prior written permission.\n *\n * THIS SOFTWARE IS PROVIDED BY THE AUTHOR ``AS IS'' AND ANY EXPRESS OR\n * IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES\n * OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED.\n * IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT,\n * INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT\n * NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,\n * DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY\n * THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT\n * (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF\n * THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.\n*/"
      }, {
        "licenseId" : "LicenseRef-Beerware-4.2",
        "comment" : "The beerware license has a couple of other standard variants.",
        "extractedText" : "\"THE BEER-WARE LICENSE\" (Revision 42):\nphk@FreeBSD.ORG wrote this file. As long as you retain this notice you\ncan do whatever you want with this stuff. If we meet some day, and you think this stuff is worth it, you can buy me a beer in return Poul-Henning Kamp",
        "name" : "Beer-Ware License (Version 42)",
        "seeAlsos" : [ "http://people.freebsd.org/~phk/" ]
  }, {

  }, 
```

##### Relationships between SPDX elements information section

```
{                                             **相较SPDX额外作为必选** **对应NTIA中的Relationship和Other Component Relationships**
    "spdxElementId" : "SPDXRef-Package",      **通过此字段来表达动静态依赖关系。**
    "relationshipType" : "DYNAMIC_LINK",
    "relatedSpdxElement" : "SPDXRef-Saxon"
  }, {
    "spdxElementId" : "SPDXRef-JenaLib",    **后续通过此字段来表达软件中的包含关系如A软件代码仓中包含B软件成分。**
    "relationshipType" : "CONTAINS",
    "relatedSpdxElement" : "SPDXRef-Package"
  }， {
    "spdxElementId" : "SPDXRef-SOURCE-openXXX",
    "relationshipType" : "VARIANT_OF",      **后续通过此字段来表达三方软件在OpenHarmony的衍生版本。**
    "relatedSpdxElement" : "SPDXRef-UPSTREAM-openXXX"
  }，
 {
    "spdxElementId" : "SPDXRef-Package-A",
    "relationshipType" : "DEPENDS_ON",      **后续通过此字段来表达A依赖B。**
    "relatedSpdxElement" : "SPDXRef-Package-B" 
  }
 {
    "spdxElementId" : "SPDXRef-bin-A",
    "relationshipType" : "GENERATED_FROM",      **后续通过此字段来构建关系。**
    "relatedSpdxElement" : "SPDXRef-Source-B" 
  }

}

```

#### OpenHarmony典型场景下SPDX格式的表达规范
##### Source SBOM的表达规范
1. OpenHarmony自研部件自身表达

```
"packages" : [ {
    "SPDXID" : "SPDXRef-SOURCE-ability_ability_base",    **源码仓： SPDXRef-SOURCE-源码仓名** 
    "filesAnalyzed" : "true",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "ability_base",                 **部件名**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **源码使用下载后的源码路径，可选**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony**
    "downloadLocation" : "https://gitee.com/openharmony/ability_ability_base/repository/archive/OpenHarmony-v5.0-Beta1",   **源码仓下载地址，可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],
    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "Apache-2.0",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseDeclared" : "Apache-2.0",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  可多行
    "description" : "元能力的基础定义部件", **部件功能描述信息，优选英文**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/ability_ability_base@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "FRAMEWORK", **相较SPDX额外作为必选**， 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为本代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为本代码仓对应tagEOS时间
}]
```
2. OpenHarmony第三方部件与上游软件衍生关系表达（此场景为该部件就是上游主软件的鸿蒙化编译适配,本部件时上游部件的一个衍生作品，如third_party_libuv部件是libuv软件的鸿蒙化适配作品。本场景是社区使用第三方软件的主要场景，原则上一个部件就是一款软件，如果有多款应该拆分）

```
"packages" : [ {
    "SPDXID" : "SPDXRef-SOURCE-third_party_libuv",    **源码仓： SPDXRef-SOURCE-源码仓名** 
    "filesAnalyzed" : "true",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "third_party_libuv",                 **部件名**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发，第三方软件亦是由OpenHarmony仓库托管分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **源码使用下载后的源码路径，可选**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony**
    "downloadLocation" : "https://gitee.com/openharmony/third_party_libuv/repository/archive/OpenHarmony-v5.0-Beta1",   **源码仓下载地址，可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeExcludedFiles" : [ "./package.spdx" ],
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],

    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "(LGPL-2.0-only OR LicenseRef-3)",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseInfoFromFiles" : [ "GPL-2.0-only", "LicenseRef-2", "LicenseRef-1" ],   **合规必选****相较SPDX额外作为必选**，作为推论许可证中的参考依据，应包含组件中全量许可证信息，在此不做许可证间关系说明，由工具扫描文件级许可证，必须为SPDX License Expression
    "licenseDeclared" : "(LGPL-2.0-only AND LicenseRef-3)",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "licenseComments" : "The license for this project changed with the release of version x.y.  The version of the project included here post-dates the license change.",   **合规必选**
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  可多行
    "description" : "The GNU C Library defines functions that are specified by the ISO C standard.", **部件功能描述信息，开源管理必选**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/ability_ability_base@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       },   {
      "referenceCategory" : "SECURITY",
      "referenceLocator" : "cpe:2.3:a:pivotal_software:spring_framework:4.1.0:*:*:*:*:*:*:*",
      "referenceType" : "cpe23Type"
      }],
    "primaryPackagePurpose" : "SOURCE", **相较SPDX额外作为必选** **开源管理必选**, 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为本代码仓对应tag发布时间，非上游地址时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为本代码仓对应tagEOS时间，非上游地址时间
}，
{
    "SPDXID" : "SPDXRef-UPSTREAM-libuv",        ** 源码仓：SPDXRef-SOURCE-源码仓名 ** 
    "name" : "libuv",                           ** 上游软件名 **
    "supplier" : "Organization: XXX",           ** 上游软件分发供应商 **
    "versionInfo" : "v1.48.0"                   ** 上游软件原生版本号 **，
    "originator" : "Organization: XXX (contact@example.com)",  ** 上游原始供应商，和分发商可能不一致 **
    "downloadLocation" : "https://github.com/libuv/libuv/archive/refs/tags/v1.44.2.tar.gz",   ** 上游源码包下载地址 **
    "homepage" : "https://libuv.org/",          ** 填写上游软件首页地址 **
    "licenseConcluded" : "(LGPL-2.0-only OR LicenseRef-3)",  ** 由SBOM创建者推论的该软件的许可证信息，扫描工具，必须为SPDX License Expression** 
    "licenseDeclared" : "(LGPL-2.0-only AND LicenseRef-3)",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  ** 可多行 **
    "description" : "The GNU C Library defines functions that are specified by the ISO C standard.", **上游软件功能描述，开源管理必选**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:github/libuv/libuv@v1.48.0",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "LIBRARY", **相较SPDX额外作为必选** **开源管理必选**, 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为上游代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为上游代码仓对应tagEOS时间

}],
"relationships":[
 {
    "spdxElementId" : "SPDXRef-SOURCE-third_party_libuv",
    "relationshipType" : "VARIANT_OF",      **后续通过此字段来表达三方软件在OpenHarmony的衍生版本。**
    "relatedSpdxElement" : "SPDXRef-UPSTREAM-libuv"
  }]
```

3.  OpenHarmony中自研/三方部件中包含一款或多款上游开源软件的关联表达方式（此场景为特殊少量场景，原则上，自研部件不应包含第三方成分，但部分特殊自研或三方部件无法再拆分的，部件中源码包含一个或多个上游软件成分，如device_soc_XXX 中包含其他第三方开源软件）


```
"packages" : [ {
    "SPDXID" : "SPDXRef-SOURCE-device_soc_XXX",    **源码仓： SPDXRef-SOURCE-源码仓名** 
    "filesAnalyzed" : "true",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "device_soc_XXX",                 **部件名**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发，第三方软件亦是由OpenHarmony仓库托管分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **源码使用下载后的源码路径，可选**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony**
    "downloadLocation" : "https://gitee.com/openharmony/device_soc_XXX/repository/archive/OpenHarmony-v5.0-Beta1",   **源码仓下载地址，可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeExcludedFiles" : [ "./package.spdx" ],
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],

    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "(LGPL-2.0-only OR LicenseRef-3)",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseInfoFromFiles" : [ "GPL-2.0-only", "LicenseRef-2", "LicenseRef-1" ],   **可选，合规必选****相较SPDX额外作为必选**，作为推论许可证中的参考依据，应包含组件中全量许可证信息，在此不做许可证间关系说明，由工具扫描文件级许可证，必须为SPDX License Expression
    "licenseDeclared" : "(LGPL-2.0-only AND LicenseRef-3)",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "licenseComments" : "The license for this project changed with the release of version x.y.  The version of the project included here post-dates the license change.",   **合规必选**
    "copyrightText" : "Copyright 2008-2010 John Smith",   **可选，合规必选**  可多行
    "description" : "The GNU C Library defines functions that are specified by the ISO C standard.", **部件功能描述信息，开源管理必选**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/device_soc_XXX@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "DEVICE", **相较SPDX额外作为必选** **开源管理必选**, 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为本代码仓对应tag发布时间，非上游地址时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为本代码仓对应tagEOS时间，非上游地址时间
}，
{
    "SPDXID" : "SPDXRef-UPSTREAM-libuv",        ** 源码仓：SPDXRef-SOURCE-源码仓名 ** 
    "name" : "libuv",                           ** 上游软件名 **
    "supplier" : "Organization: XXX",           ** 上游软件分发供应商 **
    "versionInfo" : "v1.48.0"                   ** 上游软件原生版本号 **，
    "originator" : "Organization: XXX (contact@example.com)",  ** 上游原始供应商，和分发商可能不一致 **
    "downloadLocation" : "https://github.com/libuv/libuv/archive/refs/tags/v1.44.2.tar.gz",   ** 上游源码包下载地址 **
    "homepage" : "https://libuv.org/",          ** 填写上游软件首页地址 **
    "licenseConcluded" : "(LGPL-2.0-only OR LicenseRef-3)",  ** 由SBOM创建者推论的该软件的许可证信息，扫描工具，必须为SPDX License Expression** 
    "licenseDeclared" : "(LGPL-2.0-only AND LicenseRef-3)",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  ** 可多行 **
    "description" : "The GNU C Library defines functions that are specified by the ISO C standard.", **上游软件功能描述，开源管理必选**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:github/libuv/libuv@v1.48.0",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "LIBRARY", **相较SPDX额外作为必选** **开源管理必选**, 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为上游代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为上游代码仓对应tagEOS时间

}，
{
    "SPDXID" : "SPDXRef-UPSTREAM-zlib",        ** 源码仓：SPDXRef-SOURCE-源码仓名 ** 
    "name" : "zlib",                           ** 上游软件名 **
    "supplier" : "Organization: XXX",           ** 上游软件分发供应商 **
    "versionInfo" : "v1.2.13"                   ** 上游软件原生版本号 **，
    "originator" : "Organization: XXX (contact@example.com)",  ** 上游原始供应商，和分发商可能不一致 **
    "downloadLocation" : "https://github.com/madler/zlib/releases/download/v1.2.13/zlib-1.2.13.tar.gz",   ** 上游源码包下载地址 **
    "homepage" : "https://www.zlib.net/",          ** 填写上游软件首页地址 **
    "licenseConcluded" : "zlib",  ** 由SBOM创建者推论的该软件的许可证信息，扫描工具，必须为SPDX License Expression** 
    "licenseDeclared" : "(LGPL-2.0-only AND LicenseRef-3)",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  ** 可多行 **
    "description" : "The GNU C Library defines functions that are specified by the ISO C standard.", **上游软件功能描述，开源管理必选**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:github/madler/zlib@vv1.2.13",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "LIBRARY", **相较SPDX额外作为必选** **开源管理必选**, 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为上游代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为上游代码仓对应tagEOS时间

}],
"relationships":[
 {
    "spdxElementId" : "SPDXRef-SOURCE-device_soc_XXX",
    "relationshipType" : "CONTAINS",                     ** device_soc_XXX 包含libuv**
    "relatedSpdxElement" : "SPDXRef-UPSTREAM-libuv"
  }，
 {
    "spdxElementId" : "SPDXRef-SOURCE-device_soc_XXX",
    "relationshipType" : "CONTAINS",                     ** device_soc_XXX 包含zlib**
    "relatedSpdxElement" : "SPDXRef-UPSTREAM-zlib"
  }


]
```


4. OpenHarmony中部件与部件间存在动态链接或者调用关系而产生依赖的关联表达

```
"packages" : [ {
    "SPDXID" : "SPDXRef-SOURCE-ability_ability_base",    **源码仓： SPDXRef-SOURCE-源码仓名** 
    "filesAnalyzed" : "true",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "ability_base",                 **部件名**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **源码使用下载后的源码路径，可选**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony**
    "downloadLocation" : "https://gitee.com/openharmony/ability_ability_base/repository/archive/OpenHarmony-v5.0-Beta1",   **源码仓下载地址，可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],
    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "Apache-2.0",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseDeclared" : "Apache-2.0",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  可多行
    "description" : "元能力的基础定义部件", **部件功能描述信息，优选英文**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/ability_ability_base@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "FRAMEWORK", **相较SPDX额外作为必选**， 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为本代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为本代码仓对应tagEOS时间
}，
{
    "SPDXID" : "SPDXRef-SOURCE-ability_ability_runtime",    **源码仓： SPDXRef-SOURCE-源码仓名** 
    "filesAnalyzed" : "true",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "ability_base",                 **部件名**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **源码使用下载后的源码路径，可选**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony**
    "downloadLocation" : "https://gitee.com/openharmony/ability_ability_runtime/repository/archive/OpenHarmony-v5.0-Beta1",   **源码仓下载地址，可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],
    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "Apache-2.0",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseDeclared" : "Apache-2.0",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  可多行
    "description" : "元能力的基础定义部件", **部件功能描述信息，优选英文**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/ability_ability_runtime@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "FRAMEWORK", **相较SPDX额外作为必选**， 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为本代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为本代码仓对应tagEOS时间
}]，
"relationships":[
 {
    "spdxElementId" : "SPDXRef-SOURCE-ability_ability_runtime",
    "relationshipType" : "DEPENDS_ON",                     ** runtime依赖base **
    "relatedSpdxElement" : "SPDXRef-SOURCE-ability_ability_base"
  }
]
```



##### Build SBOM的表达规范

1. OpenHarmony二进制自身表达

```
{
	"SPDXID":"SPDXRef-system-lib-libability_base.so"
    "filename":"/system/lib/libdXXX.so"      **构建SBOM必选**    
    "checksums": [
        {
			"algorithm":"SHA1",
            "checksumValue": "279XXXXXXXXXXXXXXXXXXXX"
        }
    ]
}
```
2. 二进制与产品镜像的关系表达(通过hasFile表达)

```
"packages" : [ {
    "SPDXID" : "SPDXRef-PRODUCT",    **二进制仓： 路径 system/lib/libability_base.so** 
    "filesAnalyzed" : "ture",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "Dayu200",                 **二进制名称**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **二进制路径**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony** 
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ], 
    "hasFiles":[                                          ** 镜像包与二进制的包含关系  **
         "SPDXRef-system-lib-libability_base.so",        
         "SPDXRef-system-lib-libability_runtime.so"
         "XXXXXXX"
     ]
    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "primaryPackagePurpose" : "OPERATING-SYSTEM", **相较SPDX额外作为必选**， 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
}，
{
	"SPDXID":"SPDXRef-system-lib-libability_base.so"
    "filename":"/system/lib/libdXXX.so"      **构建SBOM额外作为必选**
    "checksums": [
        {
			"algorithm":"SHA1",
            "checksumValue": "279XXXXXXXXXXXXXXXXXXXX"
        }
    ]
}
]
```

3. OpenHarmony二进制自身与产品大包的关系已及二进制源码仓溯源关系表达

```
"packages" : [ {
    "SPDXID" : "SPDXRef-PRODUCT",    **二进制仓： 路径 system/lib/libability_base.so** 
    "filesAnalyzed" : "ture",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "Dayu200",                 **二进制名称**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **二进制路径**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony** 
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ], 
    "hasFiles":[                                          ** 镜像包与二进制的包含关系  **
         "SPDXRef-system-lib-libability_base.so",        
         "SPDXRef-system-lib-libability_runtime.so"
         "XXXXXXX"
     ]
    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "primaryPackagePurpose" : "OPERATING-SYSTEM", **相较SPDX额外作为必选**， 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
}，
{
	"SPDXID":"SPDXRef-system-lib-libability_base.so"
    "filename":"/system/lib/libdXXX.so"      **构建SBOM额外作为必选**
    "checksums": [
        {
			"algorithm":"SHA1",
            "checksumValue": "279XXXXXXXXXXXXXXXXXXXX"
        }
    ]
},
{
    "SPDXID" : "SPDXRef-SOURCE-ability_ability_base",    **源码仓： SPDXRef-SOURCE-源码仓名** 
    "filesAnalyzed" : "true",     **此字段为true，即可以基于此组件进行文件级分析**
    "name" : "ability_base",                 **部件名**
    "supplier" : "Organization: OpenHarmony",     **当前OpenHarmony的源，均为OpenHarmony分发**
    "versionInfo" : "OpenHarmony-4.0-Release"  **OpenHarmony社区大版本号**，
    "PackageFileName"："./myrootdir/mysubdir1" **源码使用下载后的源码路径，可选**
    "originator" : "Organization: OpenHarmony (contact@example.com)",  **源码仓的原始供应商，全部填写OpenHarmony**
    "downloadLocation" : "https://gitee.com/openharmony/ability_ability_base/repository/archive/OpenHarmony-v5.0-Beta1",   **源码仓下载地址，可按以下方式git地址+tag点方式，若无tag点，可以使用分支 "git+https://git.myproject.org/MyProject.git@v1.0"
    "packageVerificationCode" : {                                           当 filesAnalyzed为true时，填写以下字段，当 filesAnalyzed为false时，不填写
      "packageVerificationCodeValue" : "d6a770ba38583ed4bb4525bd96e50461655d2758"
    }
    "checksums" : [ {                        **相较SPDX额外作为必选**， **对应NTIA中的Component Hash**， 同packageVerificationCode
      "algorithm" : "SHA1",
      "checksumValue" : "2fd4e1c67a2d28fced849ee1bb76e7391b93eb12"
    } ],
    "homepage" : "https://www.openharmony.cn/mainPlay",   **相较SPDX额外作为必选**，统一填OpenHarmony首页https://www.openharmony.cn/mainPlay
    "licenseConcluded" : "Apache-2.0",  **相较SPDX额外作为必选** **对应NTIA中的License Information** 由SBOM创建者推论的该组件的许可证信息，可借助扫描工具，必须为SPDX License Expression
    "licenseDeclared" : "Apache-2.0",    **合规必选****相较SPDX额外作为必选**，仅包含原始作者对许可证的声明，不包含第三方库的许可证信息。
    "copyrightText" : "Copyright 2008-2010 John Smith",   **合规必选**  可多行
    "description" : "元能力的基础定义部件", **部件功能描述信息，优选英文**
    "externalRefs" : [ {     **相较SPDX额外作为必选**, **对应NTIA中的Unique Identifier** 
      "referenceCategory" : "PACKAGE-MANAGER",
      "referenceLocator" : "pkg:gitee/openharmony/ability_ability_base@OpenHarmony-v4.0-Release",
      "referenceType" : "purl"
       }],
    "primaryPackagePurpose" : "FRAMEWORK", **相较SPDX额外作为必选**， 标识软件包属性，应用hap使用APPLICATION;应用框架使用FRAMEWORK; 单一功能库使用LIBRARY;容器镜像使用CONTAINER; 操作系统OS使用OPERATING-SYSTEM;芯片及开发板相关使用DEVICE;驱动等底软使用 FIRMWARE， 当前组件为多个源码文件的集合使用SOURCE; 当前为压缩包(.tar, .zip等）使用ARCHIVE; 独立可分发的单文件使用FILE ; 如果仅用于安装软件的工具使用INSTALL，未被上述领域覆盖的使用OTHER.
    "releaseDate" : "2012-01-29T18:30:22Z",  **开源管理必选**  版本发布时间，此处为本代码仓对应tag发布时间
    "validUntilDate" : "2014-01-29T18:30:22Z",  ***开源管理必选**  EOS时间 此处为本代码仓对应tagEOS时间
} ]
"relationships":[
 {
    "spdxElementId" : "SPDXRef-system-lib-libability_base.so",
    "relationshipType" : "GENERATED_FROM",                     ** 构建生成关系 **
    "relatedSpdxElement" : "SPDXRef-SOURCE-ability_ability_base"
  }
]
```

4. 依赖关系与衍生关系的追溯同Source BOM 见上一节所示.


#### cycloneDX格式的表达方式规范

cycloneDX 1.5 json格式

```
{
 "bomFormat":"CycloneDX",
 "specVersion": "1.5",
 "serialNumber":"urn:uuid:3e671687-395b-41f5-a30f-a58921a69b79""   **相较CycloneDX额外作为必选**， 唯一标识
 "version"：“1” **相较CycloneDX额外作为必选**， 用作标识对已有SBOM的修改版本信息
 "metadata":{
   "timestamp": "2024-03-17 18:00:00",   **相较CycloneDX额外作为必选**,**对应NTIA中Timestamp**
   "lifecycles": "design" **对应NTIA中Lifecycle Phase**    design/pre-build/build/post-build/operations/discovery/decommission https://cyclonedx.org/docs/1.5/json/#metadata_lifecycles
   "supplier": {
      "name":"OpenHarmony"      **相较CycloneDX额外作为必选**， **对应NTIA中的Supplier Name**，实际分发者，不一定与原始分发者一致，不能只是分发网站，要对应组织名，当前OpenHarmony的源，均为OpenHarmony分发，第三方软件亦是由OpenHarmony仓库托管分发
     } 
  }
"components":{
  [{"type":"library",   application/framework/library/container/platform/operating-system/device/device-driver/firmware/file/machine-learning-model/data
    "suppiler": {
      "name":"OpenHarmony"      **相较CycloneDX额外作为必选**， **对应NTIA中的Supplier Name**，实际分发者，不一定与原始分发者一致，不能只是分发网站，要对应组织名，当前OpenHarmony的源，均为OpenHarmony分发，第三方软件亦是由OpenHarmony仓库托管分发
      } ,
    "author":" Inc",
    "name":"tomcat-catalina",
    "version":"9.0.14" **相较CycloneDX额外作为必选**，**对应NTIA中的Version of the Component**组件版本信息，用于表示版本变化，
    "hashes": {
        "alg": "SHA-256",
        "content": "3942447fac867ae5cdb3229b658f4d48"
      },
    "licenses":[{
       "license":{
        "id": "Apache-2.0",   **相较CycloneDX额外作为必选**,以spdxid为准
         }, 
       },{}]，
    "copyright":"XXXX Inc",
    "cpe":"cpe:2.3:a:acme:component_framework:-:*:*:*:*:*:*:*",
    "purl"："pkg:maven/com.acme/tomcat-catalina@9.0.14?packaging=jar"，
    "pedigree": {     **相较CycloneDX额外作为必选，要求第三方软件必选** **对应NTIA中的Other Component Relationships**
        "ancestors":{Component object},  找到fork的上游软件，并进行描述，如果遇到openEuler小包，则在ancestors内，进一步嵌套找到上游软件。
        "variants":{Component object}, 识别不清具体关系的放在此处，但是知道有相关性，可以用于工具中的成分识别
        "commits":[{
         "uid":"commit id",
         "url": "",
         "message": "content of commit"
         },{
         ...
          }
        ],
        "patches":[{
         "type":"backport",  unofficial/monkey/backport/cherry-pick
         "diff": "text",
         "resolves": {
            "type": "defect"  defect/enhancement/security
            "id":""
          }
          },{}]
        }    
    }, {
    ....
   }
  ] 
 } 
}


```




