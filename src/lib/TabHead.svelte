<script lang='ts'>
	export let tabStyle: 'default' | 'underline' ='default'
	type classOptions = {
		[key: string]: string;
	}
	export const divClasses = {
		default: 'mb-4 border-b border-gray-200 dark:border-gray-700',
    underline:
      'mb-4 text-sm font-medium text-center text-gray-500 border-b border-gray-200 dark:text-gray-400 dark:border-gray-700'
	}
	export const ulClasses = {
		default: 'flex flex-wrap -mb-px',
    underline: 'flex flex-wrap -mb-px'
	}
</script>

<div class={divClasses[tabStyle]}>
	<ul class={ulClasses[tabStyle]}  role="tablist">
		<slot />
	</ul>
</div>
