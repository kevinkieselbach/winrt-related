---
Description: ProductFeatures
MS-HAID: StoreManifest.element\_ProductFeatures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/apps
Search.Product: eADQiWindows 10XVcnh
title: ProductFeatures
ms.assetid: 95f2ec1b-e3d1-490d-a5dc-367e385f7fc5
author: laurenhughes
ms.author: lahugh
keywords: windows 10
---

# ProductFeatures


The ProductFeatures element is the container for all existing and future product features that will be configured through the StoreManifest XML file.

## Element hierarchy

<dl>
<dt><a href="element-storemanifest.md">&lt;StoreManifest&gt;</a></dt>
<dd><b>&lt;ProductFeatures&gt;</b></dd>
</dl>

## Syntax

``` syntax
<ProductFeatures>

  <!-- Child elements -->
  ( DeviceCompanionApplication?
  & ExclusiveOptOut?
  & PreinstallOptOut?
  )

</ProductFeatures>
```

### Key

`?`   optional (zero or one)
`&`   interleave connector (may occur in any order)

## Attributes and Elements


### Attributes

None.

### Child Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Child Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[DeviceCompanionApplication](element-devicecompanionapplication.md)</td>
<td><p>The DeviceCompanionApplication element contains all the configuration required to declare your app as a Windows Store device app.</p></td>
</tr>
<tr class="even">
<td>[ExclusiveOptOut](element-exclusiveoptout.md)</td>
<td><p>Do not use. The ExclusiveOptOut element is no longer read by the Windows Store.</p></td>
</tr>
<tr class="odd">
<td>[PreinstallOptOut](element-preinstalloptout.md)</td>
<td><p>Do not use. The PreinstallOptOut element is no longer read by the Windows Store.</p></td>
</tr>
</tbody>
</table>

 

### Parent Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[StoreManifest](element-storemanifest.md)</td>
<td><p>Root node for the StoreManifest schema (for Windows 8.1 and earlier).</p></td>
</tr>
</tbody>
</table>

 

## Remarks

The StoreManifest schema allows the ProductFeatures element to be empty. If so, the StoreManifest.xml will have no effect at app onboarding (as if no StoreManifest.xml was submitted with the app).

## Examples

The following is an example of the ProductFeatures element that declares the app as a device app.

```XML
<ProductFeatures>     
    <DeviceCompanionApplication>
        <ExperienceIds>
            <ExperienceId>aeabdaa8-3bcd-4f03-a7f5-54647fd574c2</ExperienceId>
        </ExperienceIds>
    </DeviceCompanionApplication>   
</ProductFeatures>
```

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/2010/StoreManifest</p></td>
</tr>
</tbody>
</table>

 

 


