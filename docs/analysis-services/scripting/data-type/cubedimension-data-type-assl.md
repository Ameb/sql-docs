---
title: "CubeDimension Data Type (ASSL) | Microsoft Docs"
ms.date: 05/03/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: assl
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
---
# CubeDimension Data Type (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
  Defines a primitive data type that represents the relationship between a dimension and a cube.  
  
## Syntax  
  
```xml  
  
<CubeDimension>  
      <ID>...</ID>  
   <Name>...</Name>  
   <Translations>...</Translations>  
   <DimensionID>...</DimensionID>  
   <Visible>...</Visible>  
   <AllMemberAggregationUsage>...</AllMemberAggregationUsage>  
   <HierarchyUniqueNameStyle>...</HierarchyUniqueNameStyle>  
   <MemberUniqueNameStyle>...</MemberUniqueNameStyle>  
      <Attributes>...</Attributes>  
   <Hierarchies>...</Hierarchies>  
      <Annotations>...</Annotation>  
</CubeDimension>  
```  
  
## Data Type Characteristics  
  
|Characteristic|Description|  
|--------------------|-----------------|  
|Base data types|None|  
|Derived data types|None|  
  
## Data Type Relationships  
  
|Relationship|Element|  
|------------------|-------------|  
|Parent elements|None|  
|Child elements|[AllMemberAggregationUsage](../../../analysis-services/scripting/properties/allmemberaggregationusage-element-assl.md), [Annotations](../../../analysis-services/scripting/collections/annotations-element-assl.md), [Attributes](../../../analysis-services/scripting/collections/attributes-element-assl.md), [DimensionID](../../../analysis-services/scripting/properties/dimensionid-element-assl.md), [Hierarchies](../../../analysis-services/scripting/collections/hierarchies-element-assl.md), [HierarchyUniqueNameStyle](../../../analysis-services/scripting/properties/hierarchyuniquenamestyle-element-assl.md), [ID](../../../analysis-services/scripting/properties/id-element-assl.md), [MemberUniqueNameStyle](../../../analysis-services/scripting/properties/memberuniquenamestyle-element-assl.md), [Name](../../../analysis-services/scripting/properties/name-element-assl.md), [Visible](../../../analysis-services/scripting/properties/visible-element-assl.md), [Translations](../../../analysis-services/scripting/collections/translations-element-assl.md)|  
|Derived elements|[Dimension](../../../analysis-services/scripting/objects/dimension-element-assl.md) ([Dimensions](../../../analysis-services/scripting/collections/dimensions-element-assl.md) collection of [Cube](../../../analysis-services/scripting/objects/cube-element-assl.md))|  
  
## Remarks  
 There is one **CubeDimension** for each dimension relationship on a **Cube**. The **CubeDimension** covers all the **MeasureGroups** of the cube.  
  
 A **CubeDimension** must include a [CubeHierarchy](../../../analysis-services/scripting/data-type/cubehierarchy-data-type-assl.md) if the dimension has something specific to say about the hierarchy, including disabling the hierarchy (thereby, allowing selection of which hierarchies apply to a particular dimension usage), or making the hierarchy invisible.  
  
 Similarly, a **CubeDimension** must include a [CubeAttribute](../../../analysis-services/scripting/data-type/cubeattribute-data-type-assl.md) only if the dimension has something specific to say about the attribute. (There is no way to select which attributes apply to a particular dimension usage, though attributes can be made invisible).  
  
 The corresponding element in the Analysis Management Objects (AMO) object model is <xref:Microsoft.AnalysisServices.CubeDimension>.  
  
## See Also  
 [Analysis Services Scripting Language XML Data Types &#40;ASSL&#41;](../../../analysis-services/scripting/data-type/analysis-services-scripting-language-xml-data-types-assl.md)  
  
  
