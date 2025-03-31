---
title: AnchorFeature
icon: lucide:layout-list
badges:
  - value: Source
    icon: lucide:code
    to: https://github.com/ZTL-UwU/shadcn-docs-nuxt/blob/main/components/content/Accordion.vue
    target: _blank
  - value: 0.5.0
---

## Usage

::stack
  ::div{class="p-4 flex space-x-4"}
  ::anchor-feature{anchor="#test-anchor-id"}
    ::badge
    指定 id 的元素
  ::

  ::anchor-feature{anchor="0"}
    ::badge
    指定数字的元素
  ::

  ::anchor-feature{anchor=".test-anchor-class"}
    ::badge
    指定 class 的元素
  ::
  ::
  ```mdc
  ::anchor-feature{anchor="#test-anchor-id"}
    ::badge
    指定 id 的元素
  ::

  ::anchor-feature{anchor="0"}
    ::badge
    指定数字的元素
  ::

  ::anchor-feature{anchor=".test-anchor-class"}
    ::badge
    指定 class 的元素
  ::
  ```
::

## Anchor Element

::stack
  ::div{class="test-anchor my-[20vh]"}
    ::span{id="test-anchor-id"}
      指定 id 的元素
    ::

    ::span{id="anchor_0"}
      指定数字的元素
    ::

    ::span{class="test-anchor-class"}
      指定 class 的元素
    ::
  ::
  ```mdc
  ::span{id="test-anchor-id"}
    指定 id 的元素
  ::

  ::span{id="anchor_0"}
    指定数字的元素
  ::

  ::span{class="test-anchor-class"}
    指定 class 的元素
  ::
  ```
::

## Props

#### `::anchor-feature`{lang="mdc"}

::field-group
  :field{name="anchor" type="string | number" default-value="''"}[元素选择器 如果是数字进行特殊处理 `0 -> anchor_0`]
  :field{name="tag" type="string" default-value="'div"}[Default Elements]
::
