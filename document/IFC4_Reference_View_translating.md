# Foreword

To be updated from [standard foreword boiler plate text] (http://www.buildingsmart-tech.org/ifc/IFC4/final/html/foreword.htm)

# Introduction

## Purpose
With the publication of the IFC4 release, that has been accepted as ISO16739 by the International Standardization Organization, several enhancements and improvements over the previous IFC releases are now available for improved open BIM interoperability using the IFC protocol.

The main purpose of this document is to define a standardized subset of the IFC4 schema, a Model View Definition MVD, that is particularly suitable for all BIM workflows that are based on reference models, where the exchange is mainly one-directional. Here requested modifications of the BIM data, mainly of the shape representation, are handled by a change request to the original author, and changes are not executed upon the imported IFC data with the intent to be sent back to the original source.

本文档的主要意图在于定义一个标准化的IFC4 Schema子集，即Model View Definition (MVD)，该子集将十分适用于所有基于参照模型(reference model wiki:http://en.wikipedia.org/wiki/Reference_model)的、切主要为单方向交换的BIM工作流程。（不明：Here requested modifications of the BIM data, mainly of the shape representation, are handled by a change request to the original author, and changes are not executed upon the imported IFC data with the intent to be sent back to the original source.）

Examples of this reference workflow are:
可以参考的工作流程的例子如下：
- Coordination planning (combining different discipline specific IFC models for visual checking)
调度规划（组合来自不同学科的特定IFC模型用于可视化检查）

- Clash detection (finding clashes between different discipline specific IFC models)
冲突检查（找到不同学科的特定IFC模型之间的冲突）

- Background reference (loading an IFC model, usually from a different discipline) as a linked model
以链接模型的方式进行后台引用（IFC模型通常来至于不同的学科）

- Quantity take-off (determine the quantities of the various model elements with the IFC model)
工程量清单（测量基于IFC模型的多重类型的模型元素的工程量）

- Construction sequencing (taking the IFC model and associating it to a construction schedule)
建造顺序（将IFC模型编入建筑计划）

- Visual presentation (for presenting the IFC model to a broad audience)
可视化表现（展示IFC模型给更广泛的对象）

Common characteristics of the workflow using reference models are:

使用参照模型的工作流程所具备的共同特性如下：

- The source of the BIM information remains with the originator
BIM信息的来源属于创作者

- The full parametric behaviour, and thereby the intellectual engineering property, remains with the originator
完全参数化行为（？），及其知识工程的产权属于创作者


- The ownership of the model, and responsibility for its correctness, remains with the originator 
模型的所有权与保证其正确性的责任归于创作者

- The original model is published as IFC4 Reference View model reflecting the as-is status
所有作为IFC4 Reference view model发布的原始模型都处于免责状态

- The receiver of the IFC4 Reference View model has access to the full model content
所有IFC4 Reference View model的接收者都能够得到完全的模型内容

- The receiver of the IFC4 Reference View is not supposed to modify the model
所有IFC4 Reference View model的接收者不被允许更改这些模型

- The receiver of the IFC4 Reference View can analyse and extract the information of the model
所有IFC4 Reference View model的接收者可以分析或者取出模型的信息

- If the receiver suggests or demands a change, it has to be communicated as a change request to the originator
如果接收者建议或者要求变更模型，这个修改请求将会发送给该模型的创作者

- The buildingSMART standard BCF (BIM Collaboration Format) is developed to efficiently support these change requests. 
BCF格式是一个buildingSMART标准，将用于提高这些修改请求的效率

The Level of Detail of the shape representation and the Level of Information for the property content of the actual reference models depends on the source model. The buildingSMART standard IDM (Information Delivery Manual) can be used to determine the minimum content for a particular workflow support. The IFC4 Reference View allows rich content to be published, see next chapter Objective for more details. 
实际参照模型的造型表达的层次细节与属性内容的信息化程度完全取决于原始模型，IDM可以被用于确定支持特定的工作流程的最少内容。IFC4 Reference View允许发布富内容。

## Objective
The main objective of the IFC Reference View is the widest possible proliferation of IFC BIM data across a big range of software application types supporting different communication and collaboration workflows.
IFC Reference View的目标在于帮助可能会通过大量一系列的应用程序类型广泛增殖的IFC BIM数据支持不同的沟通与合作的工作流程。

The IFC Reference View is characterized by the ability to publish BIM data following that subset of IFC definitions that enables semantically rish(rich) content of building data, and to some degree also other built environment data, to be exchanges with a streamlined geometric representation that is optimized for analysis and display, but excludes dimension-driven geometric parameters. The geometric representation is therefore suitable for all workflow scenarios, where the imported IFC model is displayed, analysed, compared, clashed, but not parametricly modified for futher work processes.
IFC Reference View的特征是具备一种发布遵循IFC定义子集的BIM数据的能力，这种数据是一种能够提供为建筑数据提供语义的富内容。在某种程度上来说，该能力可以将其他的建筑环境数据将会被置换为专门为分析与显示优化过的流线几何表现，但是不包含维度驱动的几何参数。这种几何表现十分的适合当导入的IFC模型处于显示、分析、比较、冲突的工作流程场景之下，但是却不适合在未来的过程中进行参数化修改。

Semantic building data models being exchanged using the IFC4 Reference View would typically include:
基于IFC4 Reference View之下被交换的语义建筑数据模型包含：

- physical elements with explicit geometry, properties, quantities, material, and classification
明确定义了几何、属性、工程量、材料、与类别的物理元素

- types of elements with associated physical elements to group common definitions (geometry, properties, material, and classification)
用于关联物理元素与分组共同的定义的那些元素的类型

- spatial elements (spaces, zones) with explicit geometry, properties, quantities, and classification
明确定义了集合、属性、工程量与类别的空间元素

- spatial structure elements (site, building, story), but also spatial zones for non-vertical construction
空间结构元素，也包含空间区域，用于非垂直建造过程。

- element breakdown structure between physical elements (assemblies, sub-assemblies, parts)
物理元素之间的元素分解结构（装配，子装配，部件）

- spatial breakdown structure between spatial elements (spatial decomposition of building, story(storey) or zones)
空间元素之间的空间分解结构（建筑的空间分解，楼层与区域）

- spatial containment structure between spatial elements and physical elements (elements in spatial zone)
空间元素与物理元素之间的空间的包含结构（元素如何置于空间区域中）

- logical system structure and assignment (physical elements assigned to systems and sub systems)
逻辑系统的结构与分配（将物理元素分配到系统或者子系统中去）

- topological structure of system networks (element to port, and port to port, relationship)
基于括扑结构的系统网络（元素到端口，端口到端口，的关系）

- common context of the building model, providing units, coordinate system and GIS positions
一些建筑模型的共用的环境，提供单位、坐标体系、GIS地址的支持

- general object identification using globally unique identifier
基于GUID的对象识别系统

Additional capabilities for enriching the semantic information exposed by the IFC4 Reference View can be defined as an Add-on Model View Definition. Forseeable examples are capturing 4D models with the addition of the work schedule related entities, or 5D models with the addition of construction resource related entities.
为了为那些被IFC4 Reference View所暴露出来的逐渐增大的语义信息提供额外能力，它们可以被定义为一种附加式的MVD。可以预见的例子包括添加与工作日程相关的实体用以捕获4D模型，或者在加上与建造资源相关的实体生成5D模型。

## Workflow support
The overall goal of the IFC Reference View is to provide workflows where building information models are to be consumed by the widest array of software applications that do not require modifying geometry. Such applications enable viewing, estimating, building, operating, and other downstream analysis. 
IFC Refence View的总目标在于提供一些工作流程，让大量的应用程序可以使用建筑信息模型，而无须修改几何数据。这些应用程序可以做到查看、估算、建筑、操作、或者其他的一些下行分析功能。

> EXAMPLE One target scenario is an architect providing building design information to a contractor or facility manager. It is expected that the resulting geometry would reflect sufficient realism for viewing in software (dimensions, normals, colors, textures), but not of rendering quality for artistic presentations (lighting, shader effects, curve interpolation, rasterizing).
例子一，目标方案是一位设计师提供建筑设计信息给一位施工人员或者设备管理者。我们期望最终提供的几何数据能够为在软件中的显示反应足够多的真实数据（尺寸，法线，色彩，贴图），而非那些为了渲染质量的艺术表达（光照，渲染特效，曲线的篡改，光栅线）

To support the widest array of consuming applications, the resulting schema should be as limited as possible for representing geometry in the interest of minimizing resources required of application developers. Such schema should also be as compact as possible to enable downstream use on mobile devices with limited network bandwidth. It is proposed that the resulting geometry is limited to triangles with normal vectors, colour and texture coordinates and simple sweeped solids with applied colour and texture.
为了支持大量的消费级应用程序，我们需要提供尽可能受到限制的表现几何，因为internet上的应用程序开发者总是尽可能的最小化资源。这种模式也需要为了下行能够使用在带宽受限的移动设备上，设计的经可能的紧凑。一个提议就是最终的几何数据将被限定在带有法线向量的三角形、色彩与贴图，和应用了色彩与贴图的简单的旋转实体之内。

## Compatibility concerns

与IFC2*3无任何兼容性，完

As the IFC4 Reference View is new (there is no corresponding concept in the IFC2x3 Coordination View), there is no constraint for compatibility, and the resulting schema will leverage new triangulation definitions in IFC4 to support more efficient data transfer.

The second Model View Definition that is proposed in parallel to the IFC4 Reference View, the IFC4 Design Transfer View, is an extension of this model view. In other words, the IFC4 Reference View is a true subset of the IFC4 Design Transfer View.

Complying software interfaces, that implements import of the IFC4 Design Transfer View, shall also be able to correctly import IFC4 Reference View data sets. But not vice versa, a complying software interface, that implements import of the IFC4 Reference View will not be capable to import IFC4 Design Transfer View data sets. It is however required that a compliant software interface for importing IFC4 Reference View displays an agreed error messange showing the IFC version, and the IFC Model View Definition of the imported IFC file, that does not match "IFC4 Reference View" with an explanation, that a non-compatible IFC file has been received.

> NOTE The correct error message and the link to further information on the buildingSMART website explaining the purpose of the different IFC Model View Deinitions need to be agreed upon.

# 1 Scope


## 1.1 General scope definition
综合scope定义

The general scope defines the main functionalities of the IFC4 Reference View as an overview. It includes a complete listing of the model elements and model element types that are included in the IFC4 Reference View MVD.
综合scope的功能是作为IFC4 Reference View的一个总览。 他包含了列表，这个列表中包含了所有IFC4 Reference View MVD所涵盖的模型元素与模型元素的类型。

> NOTE The Model elements are refered to in MVD as root concepts, being the indivudual root elements, that contain the attributes, geometric shapes, dynamic property sets and other semantic information. 
> NOTE 上文提及的模型元素在MVD中被作为root concepts.本质上是一个root元素，包含属性、集合造型、动态的属性集合与其他语义信息。

The detailed scope of the IFC4 Reference View is determined by the concept templates that are included. A detailed description of each concept template is provided by "4 Fundamental concepts and assumptions".
更加详细的scope是由IFC4 Reference View包含的concept template所决定的。关于每个concept template的详细描述请参考“4 Fundamental concepts and assumptions”。

## 1.2 Model elements
The main components of the IFC4 Reference View are the semantic model elements that carry a predefined meaning. The complete breakdown of all model elements declared in IFC4 are also known as the IFC4 built-in classification following an element by function classification.
IFC4 Reference View的主要部件是语义模型元素包含着一个预先定义的含义。在IFC4中定义的所有模型元素的完整分类同时也是IFC4内置的分类（什么？）。

In addition to each of the Model elements shown here in the subsequent tables, each Model element maybe further specialized by its "_PredefinedType_", or even a user defined type.
除了下列表格中所展示的模型元素以外，每个模型元素可能都会在不远的将来被它的“_预定义类型_”异或用户定义类型所特定化。

> EXAMPLE  An _IfcFireSuppressionTerminal_ is a specific Model element, that may be further specialized using its _PredefinedType_ Enumeration to be: a sprinkler, a hose reel, a fire hydrant, or a breeching inlet. If a proper predefined type is not yet included, a user defined type can be assigned as well.
例如说 一个_IfcFireSuppressionTerminal_是一个特定的模型元素，它可能会在将来被其自身的预定义类型枚举类型所特定化为下列一种：自动灭火喷头，消防喉头，消防龙头或者烟囱。如果没有包含任何一个合理的预定义类型，同样的用于自定义的类型也可以被分配。
 
**Architectural model elements**

| shell and core   | finishing          | furnishing
|------------------|--------------------|-----------
| _IfcBeam_        | _IfcCovering_      | _IfcFurniture_
| _IfcColumn_      | _IfcRailing_       | _IfcSystemFurnitureElement_
| _IfcChimney_ *   | _IfcShadingDevice_ | -
| _IfcRamp_ +      | _IfcCurtainWall_   | -
| _IfcStair_ ++    | _IfcDoor_          | -
| _IfcRoof_        | _IfcWindow_        | -
| _IfcSlab_        | -                  | -
| _IfcWall_        | -                  | -

> Legend: * new in IFC4, + includes IfcRampFlight, ++ includes IfcStairFlight


**Structural model elements**

| Foundation & Frame   | Reinforcement        | Fastener, etc. |
|----------------------|----------------------|----------------|
| _IfcFooting_         | _IfcReinforcingBar_  | _IfcFastener_
| _IfcPile_            | _IfcReinforcingMesh_ | _IfcMechanicalFastener_
| _IfcMember_          | _IfcTendonAnchor_    | _IfcBuildingElementPart_
| _IfcPlate_           | _IfcTendon_          | _IfcDiscreteAccessory_

> NOTE: Architectural elements, like IfcWall, IfcSlab, IfcBeam, etc, are also used in structural models, and vice versa

**Building service model elements**

The model element specialization structure within the building service domain within the IFC standard is organized 
according to its function within a distribution system, and 
not primarily according to the main building service discipline, within it is mainly used.
IFC标准里的building service领域里的模型元素的特殊化结构根据其自身的功能被组织在配水管网系统里，而不是根据首选的其主要被使用的building service学科。

The internal specialization structure for building service elements at its highest level is also independed of the fluid used within the distribution system:
这些building service元素的内部特定化结构在其最高层面上也是独立于配水管线系统中的液体的：

- flow segments
- flow fittings
- flow terminals
- flow moving devices
- flow storage devices
- flow controller
- energy conversion device
- distribution control elements

The following tables intents to assign the model elements to the various disciplines within the building service system domain.
下列表格试图分配模型元素到building service的不同的学科里面

| general MEP elements    | used for gases and fluids   | ports for connectivity |
| ------------------------|-----------------------------|------------------------|
| _IfcEngine_ *           | _IfcFlowMeter_ *            | _IfcDistributionPort_  |
| _IfcMedicalDevice_ *    | _IfcFilter_ *               | -                      |
| _IfcUnitaryEquipment_ * | -                           | -                      |


| Heating, Cooling     | Plumbing                       | Common         |
|----------------------|--------------------------------|----------------|
| _IfcBoiler_ *        | _IfcFireSuppressionTerminal_ * | _IfcPipeSegment_ *
| _IfcBurner_ *        | _IfcInterceptor_ *             | _IfcPipeFitting_ *
| _IfcCoil_ *          | _IfcSanitaryTerminal_ *        | _IfcPump_ *
| _IfcSpaceHeater_ *   | _IfcStackTerminal_ *           | _IfcValve_ *
| _IfcTubeBundle_ *    | _IfcTank_ *                    | -
| -                    | _IfcWasteTerminal_ *           | -


| Ventilation           | Air conditioning            | Common
| ----------------------|-----------------------------|-------
| _IfcAirTerminalBox_ * | _IfcAirToAirHeatRecovery_ * | _IfcDuctSegment_ *
| _IfcDamper_ *         | _IfcChiller_ *              | _IfcDuctFitting_ *
| _IfcDuctSilencer_ *   | _IfcCondenser_ *            | _IfcAirTerminal_ *
| -                     | _IfcCooledBeam_ *           | _IfcFan_ *
| -                     | _IfcCoolingTower_ *         | -
| -                     | _IfcEvaporativeCooler_ *    | -
| -                     | _IfcEvaporator_ *           | -
| -                     | _IfcHeatExchanger_ *        | -
| -                     | _IfcHumidifier_ *           | -
| -                     | _IfcCompressor_ *           | -


| Electrical                       | cont.                         | Common
|----------------------------------|-------------------------------|-------
| _IfcElectricAppliance_ *         | _IfcAudioVisualAppliance_ *   | _IfcCableSegment_ *
| _IfcElectricDistributionBoard_ * | _IfcCommunicationAppliance_ * | _IfcCableFitting_ *
| _IfcElectricGenerato_r *         | _IfcJunctionBox_ *            | _IfcCableCarrierSegment_ *
| _IfcElectricMotor_ *             | _IfcLamp_ *                   | _IfcCableCarrierFitting_ *
| _IfcElectricStorageDevice_ *     | _IfcLightFixture_ *           | -
| _IfcElectricTimeControl_ *       | _IfcSolarDevice_ *            | -
| _IfcMotorConnection_ *           | _IfcSwitchingDevice_ *        | -
| _IfcProtectiveDevice_ *          | _IfcTransformer_ *            | -


| Building automation     | cont.                               | cont.
|-------------------------|-------------------------------------|------
| _IfcActuator_ *         | _IfcFlowInstrument_ *               | _IfcSensor_ *
| _IfcAlarm_ *            | _IfcProtectiveDeviceTrippingUnit_ * | -
| _IfcController_ *       | _IfcUnitaryControlElement_ *        | -

> Legend * new in IFC4, note all building service occurrence elements are new, the previous IFC2x3 release only included the generic occurrence elements: _IfcFlowSegment_, _IfcFlowFitting_, _IfcFlowTerminal_, _IfcFlowMovingDevice_, _IfcFlowStorageDevice_, _IfcFlowController_, _IfcEnergyConversionDevice_ and _DistributionControlElement_. Those are still available as general purpose MEP Model elements, but its use is discouraged.
 

**Other model elements**

| Other elements |
|----------------|
| _IfcBuildingElementProxy_ +
| _IfcCivilElement_ *++
| _IfcGeographicElement_ *
| _IfcDistributionChamberElement_
| _IfcElementAssembly_
| _IfcTransportElement_

> Legend: * new in IFC4, + also used as general element proxy ++ provided as stub for future infrastructure extensions


**Spatial elements, spatial structure and grouping elements**

| Spatial structure   | other grouping structure   | others  |
|---------------------|----------------------------|---------|
| _IfcSpace_          | _IfcZone_                  | _IfcGrid_
| _IfcBuildingStorey_ | _IfcSystem_                | -
| _IfcBuilding_       | _IfcBuildingSystem_ *      | -
| _IfcSite_           | _IfcDistributionSystem_ *  | -
| _IfcSpatialZone_ *+ | _IfcDistributionCircuit_ * | -
| -                   | _IfcGroup_                 | -

> Legend: * new in IFC4, + provided as a stub for non vertical constructions


### 1.3 Model element types
Model element types are part of the IFC4 Reference View. They enable to describe and share common model element information that are shared by multiple occurrences of the same type. Sharable type information includes:
- Geometric shape representation;
- Property information;
- Material information.

模型元素类型是IFC Reference View的一部分。它能够描述或者共享通用的模型元素信息，这些信息是同样的类型的复数次取值所共有的。可以被共享的类型信息包含：

几何形态表达
属性信息
材料信息

> EXAMPLE: A particular air outlet as an article, with its shape, its material and its manufacturer information being described once as a type and then having several occurrences, each placed within the building, referencing the same type and hence its shape, material and properties.

例子 一个特殊的送风口同时是一件物品，拥有其造型、材料、制造商信息这些只需要将这些定义为一个类型，然后就可以使用多次。在建筑中安装的每一个送风口都指向同一个类型，可以得出它的外形、材料与一些属性。

Most of the Model elements introduced in the previous session have a corresponding Model element type, such as _IfcWall_ - _IfcWallType_, _IfcFastener_ - _IfcFastenerType_, _IfcFan_ - _IfcFanType_. Only the following spatial structure elements _IfcSite_, _IfcBuilding_, _IfcBuildingStorey_, the grouping elements _IfcGroup_, _IfcZone_, _IfcSystem_ (and subtypes), and the _IfcDistributionPort_ and _IfcGrid_ do not have matching element types.  

## 1.4 Overview on major concepts used

### 1.4.1 Object attribute
对象属性

All model elements, listed in the previous section, are defined by several generic and direct object attributes, some specific model elements do carry additional direct attributes. The usage of the direct generic attributes is defined within the following concept templates (see also Chapter 4 "fundamental concepts and assumptions"):
- "_Software Identity_", it defines how to apply the Globally Unique Id and how to compress it during exchange;
- "_User identity_", it defins the meaning of _Name_, _Description_, _LongName_ and _Tag_ attributes;
- "_Object Occurrence Predefined Type_", it defines how to use the _PredefinedType_ and in case of user defined types, how to assign the user defined type information within the _ObjectType_ attribute for occurrences of model elements;
- "_Element type predefined type_" it defines how to use the _PredefinedType_ and in case of user defined types, how to assign the user defined type information within the _ElementType_ attribute for types of model elements.
所有的在前面章节列出的模型元素都是由几个一般的，直接的对象属性所定义。有一些特殊的模型元素带有额外的直接属性。直接的泛用属性的用法有下列的concept模板所定义：
- "_Software Identity_" 定义了如何应用GUID和如何在交换的时候进行压缩处理
- "_User identity_" 它定义了_Name_, _Description_, _LongName_ and _Tag_ 这些属性的含义
-"_Object Occurrence Predefined Type_" 定义了如何使用预定义类型，如果是用户定义类型的情况下，如何通过ObjectType属性分配到模型元素中的。


### 1.4.2 Project context
There is a single instance of _IfcProject_ within each IFC data set. It sets the context for the exchange, including units, geometric context, global positioning and classification systems used within the data set. The usage of the project context is defined within the following concept templates (see also Chapter 4 "fundamental concepts and assumptions"):
每个IFC 数据集都只有一个_IfcProject.它集合了数据交换的环境，包括单位、集合环境，全球定位与数据集中使用的分类系统。project环境的用法包含在下列concept template中：

- "_Project Units_", declaration of the units used within this data set, all geometric representations are forced to use the global units (e.g. for length measure and plane angle measure), property values may override global unit declarations;
所有在数据集中使用的单位的定义。所有的集合表达都强制的使用国际标准单位。可以倍property values覆盖。

- "_Project Representation Context_", declaration of the 3D and 2D representation contexts, including precision factors;
所有3D和2D表达的环境，包含精度因素

- "_Project Global Positioning_" (new in IFC4), positioning the project engineering coordinate system (right handed Cartesian coordinate system) within a global coordinate reference system;
在全球坐标参考系中定位项目工程的坐标系统（右手笛卡尔坐标系）。

- "_Project Classification Information_", providing the name and version information about the classification systems used within the data set.
提供了在数据集中使用的分类系统的名称与版本信息

### 1.4.3 Object definition
A main objective of the IFC4 Reference View is to enable rich information content for each model element. Model element occurrences can refer to their model element types for sharing common information. General properties are attached to model elements as property sets, either directly to the model element occurrence, or to its type. Individual model element occurrences can hold their quantities, if those are pre-calculated by the sender of the IFC data set. The usage of the object definition is defined within the following concept templates (see also Chapter 4 "fundamental concepts and assumptions"):
IFC4 Reference View的一个主要目标是能够为每个模型元素提供富信息内容。每个模型元素都可以指向它的类型用于共享共通信息。共通属性会以属性集的方式附着于模型元素上，直接用于模型元素的所使用或者用于其类型。

- "_Object Typing_", associates the Model element occurrences with the corresponding element type;
使用正确的元素类型来实例化模型元素

- "_Property Sets_", assigns dynamically defined property sets, holding set of individual properties, to the model element occurrences of element type;
分配动态定义的属性集。包含着独立属性的集合。用于基于element type的model element的实例化

- "_Quantity Sets_", assigns dynamically defined quantity sets, holding set of individual quantities, to the model element occurrences.


#### 1.4.3.1 Object typing
The contept template describes the mechanism of associating model element occurrences to the corresponding type and the way and restrictions of overriding type based properties by properties directly assigned to the model element occurrences.
concept template描述了如何通过正确的类型实例化相关模型元素的机制，和一种方法，用于通过property复写类型

#### 1.4.3.2 Property sets
Property sets hold, as the name suggests, a set of properties grouped by a common theme. Each individual property has:
- a name
- an optional description
- a value, or number of values, of a given datatype
- a unit or the information of being unitless

The semantic meaning of each property is provided by its name. Properties, that are semantically declared within the scope of the IFC4 Reference View, are based on a property definition template that is published as an instrict part of the Model View Definition. Extensions to the property definitions can also be defined outside the property definition scope of the IFC4 Reference View, however the name prefix for property sets "Pset_" is restricted to properties defined within the original scope of IFC.

There are two ways to declare property templates:
- using the Property Set Definition PSD schema, an XML schema developed independent of the IFC specification,
- using the newly introduced IFC4 property set template and property template 

> NOTE The PSD Schema has been used since many earlier versions of the IFC standard and has a broad legancy. The newer property set template definitions are now part of the IFC schema and can therefore be embedded within an IFC data set directly. Both schemas can be mapped without information loss.

#### 1.4.3.3 Quantity sets
Quantity sets hold, as the name suggests, a set of quantities pre calculated for the model element occurrence. Each individual quantity has:
- a name
- an optional description
- a value of a given datatype corresponding to the quantity measure (length, area, volume, weight, time
- a unit 
- a quantity formula, describing how the quantity value was calculated

The semantic meaning of each qualtity is provided by its name. Quantities, that are semantically declared within the scope of the IFC4 Reference View, are based on a quantity definition template that is published as an instrict part of the Model View Definition. Extensions to the quantity definitions can also be defined outside the quantity definition scope of the IFC4 Reference View, however the name prefix for quantity sets "Qto_" is restricted to quantities defined within the original scope of IFC.


### 1.4.4 Object association
In addition to the Property sets and the Quantity sets, also a classification reference to an external classification system can be assigned, and material as either single material, a material constituent sets or an material layer sets aor material profile sets combining material information with dimensions can be associated to one or many model elements.

> NOTE Material dimensions are layer thicknesses, or profile geometries for e.g. a column with an embedded steel profile and a concrete protection. Within the IFC4 Reference View, such material dimensions are used exclusively as alphanumeric information, and not as part of a dimension driven parametric shape representation.

The usage of the object association is defined within the following concept templates (see also Chapter 4 "fundamental concepts and assumptions"):
- "_Material Association_"; assigns a material (or material set - constituent, layer, profile) to one or several model elements (either to  element occurrences, or as shared material information to element types).
- "_Classification Association_"; assignes a classification reference to one or several model elements.


### 1.4.5 Product shape
The first main objective of the IFC4 Reference View is to enable the exchange of highly accurate, not non-parametric, geometric representations of the model elements. Each model element is placed directly or indirectly within the project coordinate system, defining its own object coordinate system. The geometric representation items describing its shape are positioned within this object coordinate system.

In order to minimize the effort for receiving and interpreting the geometic representations by the receiving software systems, in terms of development effort, processing power and loading times, the complexity and variety of geometric models has been minimized for the IFC4 Reference View.

#### 1.4.5.1 Product placement
Each model element defines its own object coordinate system. The placement is defined by the following concept template:
- "_Local Placement_", creating an object coordinate system for the shape representation of the model element, either absolutely to the project engineering coordinate system, or relatively to another object coordination system.

#### 1.4.5.2 Product geometric representation

In scope of geometric shape representations of the 3D body geometry of physical and spatial elements are the following concept templates:
- "_Body Tessellation Geometry_", using tessellated geometry in form of triangulated tessellations for describing the body shape of the model element;
- "_Body SweptSolid Geometry_"; using extruded solid geometry or revolved solid geometry for describing the body shape of the model element;
- "_Body AdvancedSweptSolid Geometry_"; using advanced swept solid geometry of circular cross sections for describing the body shape of the model element, only the swept disk solid is in scope;

It is the default geometric representation of all model elements, allowing for a surface model representation with an indicator for closed shells (and therefore true volumes). The tessellated representation offers a very efficient way of exchanging 3D shape date, both for data set sizes and for processing time. Optionally the face normals can be exchanged as well.

Since curved shapes would lead to very densely triangulated areas, the following swept solid based representations are also in scope of the IFC4 Reference View, balancing simplicity and compactness of representation:

All other geometric models are out of scope of the IFC4 Reference View, in particular Boolean operations required for Constructive Solid Geometry CSG.

> NOTE: The IFC2x3 Coordination View included CSG capabilities, the IFC4 Reference View therefore imposes a more restricted geometric representation of model elements. The IFC4 Design Transfer View should be used, if more complex geometric representations are required by the workflow. In particular, if a dimension-driven parametric representation, used by the IFC4 standard case elements, is needed.

The geometric shape representation can either be directly assigned to a model element, or to its type. In case of type-based geometry, a the following representation type is used at the model element using the following concept template:
- "_Mapped Geometry_", mapped representation defined at the corresponding element type. A mapped representation uses Cartesian transformation operations to place the type-based geometry within its  object coordinate system.

As an exception, the following elements, _IfcGrid_ and _IfcSpace_, _IfcSpatialZone_ may have an additional foot print 2D geometry (in case of _IfcGrid_ this is the only geometric representation. It is described in the following concept template:
- "FootPrint Geometry", defining a 2D shape representation within the XY plane of the object coordinate system.

#### 1.4.5.3 Geometric presentation
Visual appearance is an important factor for the communication process using BIM data. The objective is not to support photo-realistic rendering of reference models, but to use color, basic rendering, and texture information to add visually accessible meaning to the model elements.
 
In scope of presentation capabilities for the appearance of model element shapes are the following partial concept templates:
- "_Surface Style Shading_", applying a single coloring for each solid;
- "_Surface Style Rendering_", applying a single rendering (color, transparency, reflection, etc.) for each solid; 
- "_Surface Style textures_", applying a single texture for each solid according to a texture mapping based on the solid type; 
- "_Suface style tessellation_", applying a color and/or texture for each face of a tessellated solid.

The visually adaquate presentation of model elements is constraint by the shape representation
- for tessellated geometry: color per face, texture per face
- for swept solid geometry: color and rendering information per solid, texture applied to solid using standard mapping


### 1.4.6 Object Composition

The object composition functionality describes the product breakdown structure of model elements within an IFC data set, with separate breakdown structures for physical elements and spatial elements. Physical element structures describe parts and assemblies, spatial element structures describe vertical structures (for buildings) and horizontal structures (for other assets - as a stub in this release). A specific type of decomposition is the voiding - a subtraction of a void from a physical element. Another specific type is the nesting of ports within a distribution elements.

The usage of the object association is defined within the following concept templates (see also Chapter 4 "fundamental concepts and assumptions"):
- "_Element Aggregation_", creating a hierarchical product breakdown structure relationship between assemblies and parts;  
- "_Spatial Aggregation_", creating a hierarchical spatial decomposition relationship between spatial structure elements;
- "_Element Voiding_", creating a voiding relationship between a physical element and penetrating voids - within the scope of the IFC4 Reference View this relationship is a logical relationship, the void is already part of the geometry of the physical element, 
- "_Port Nesting_", creating an 1:N relationship between the physical element and one or many ports defining inlets or outlets - used for distribution elements.


### 1.4.7 Object Assignment

The object assignment defines the assignment of objects, such as a link between model elements to groups, tasks or resources. Only the grouping assignment is in scope of the IFC4 Reference View and defined within the following concept template:
- "_Group Assignment_", Assignment of one or several model elements to a group. It includes the more specific assignments of _Grouping General_, _Grouping to System_, and _Grouping to Zones_.


### 1.4.8 Object Connectivity

The object connectivity defines the interlinkage between model elements. Examples are the link between physical elements and the spatial structure, where they are located, of the connection betwee the two ports of two consecutive distribution elements.

The usage of the object association is defined within the following concept templates (see also Chapter 4 "fundamental concepts and assumptions"):
- "_Spatial Structure_", defines the containment of a physical element within a spatial container;
- "_Port Connectivity_", defines the connection and the direction of flow between two ports of consecutive distribution elements;
- "_Building Service Connectivity_", links a spatial or distribution system to a spatial structure (such as a building section);
- "_Element Filling_", links a filling (usually a door or window) to an opening (usually in a wall or slab). 