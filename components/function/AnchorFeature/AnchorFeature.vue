<script lang="tsx">
import { defineNuxtComponent } from 'nuxt/app';
import { computed } from 'vue';
// 点击之后滚动到 当前id的位置,移除头部栏高度
export function scrollToAnchor(elOrId: string | Element) {
  const anchorElement = typeof elOrId === 'string' ? document.querySelector(elOrId) : elOrId;
  if (anchorElement) {
    const headerEl = document.querySelector('header') || document.querySelector('.h-header');
    const headerOffset = headerEl?.clientHeight || 0;
    const elementPosition = anchorElement.getBoundingClientRect().top + window.pageYOffset;
    const offsetPosition = elementPosition - headerOffset;

    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth',
    });
  }
}

export default defineNuxtComponent({
  name: 'AnchorFeature',
  props: {
    source: {
      type: Object as PropType<{ anchor: string | number }>,
      required: true,
    },
    tag: {
      type: String as PropType<'a' | 'div'>,
    },
  },
  setup(props, { slots }) {
    // /**如果 href为 0 1 2 这种数字 代表时anchor */
    const elId = computed(() => {
      const { anchor } = props.source;
      const isNotNumber = Number.isNaN(Number(anchor));
      return isNotNumber ? String(anchor) : `#anchor_${anchor}`;
    });

    // 点击之后滚动到 当前id的位置,移除头部栏高度
    return () => {
      const Tag = props.tag || 'div';
      return h(
        Tag,
        {
          class: 'cursor-pointer',
          onClick: () => {
            scrollToAnchor(elId.value);
          },
        },
        slots.default ? slots.default() : <></>,
      );
    };
  },
});
</script>
