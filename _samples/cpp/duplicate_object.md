---
title: Duplicate Object
description: Demonstrates how to make a copy of a CRhinoObject-derived object.
author: dale@mcneel.com
apis: ['C/C++']
languages: ['C/C++']
platforms: ['Windows']
categories: ['Unsorted']
origin: http://wiki.mcneel.com/developer/sdksamples/duplicateobject
order: 1
keywords: ['rhino']
layout: code-sample-cpp
---

```cpp
const CRhinoObject* object = ..... // some object
CRhinoObject* duplicate = object->Duplicate();
if( duplicate )
{
  if( context.m_doc.AddObject(duplicate) )
    context.m_doc.Redraw;
  else
    delete duplicate;
}
```