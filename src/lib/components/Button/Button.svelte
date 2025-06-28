<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { HTMLButtonAttributes } from 'svelte/elements';

	type ButtonVariant = 'default' | 'noShadow' | 'neutral' | 'reverse';
	type ButtonSize = 'default' | 'sm' | 'lg' | 'icon';

	type ButtonProps = {
		className?: string;
		variant?: ButtonVariant;
		size?: ButtonSize;
		children: Snippet<[]>;
	} & HTMLButtonAttributes;

	let {
		className = '',
		variant = 'default',
		size = 'default',
		children,
		...props
	}: ButtonProps = $props();

	let buttonClasses = [
		'inline-flex items-center justify-center whitespace-nowrap rounded-base text-sm font-base ring-offset-white transition-all gap-2 [&_svg]:pointer-events-none [&_svg]:size-4 [&_svg]:shrink-0 focus-visible:outline-hidden focus-visible:ring-2 focus-visible:ring-black focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50',
		variant === 'default' &&
			'text-main-foreground bg-main border-2 border-border shadow-shadow hover:translate-x-boxShadowX hover:translate-y-boxShadowY hover:shadow-none',
		variant === 'noShadow' && 'text-main-foreground bg-main border-2 border-border',
		variant === 'neutral' &&
			'bg-secondary-background text-foreground border-2 border-border shadow-shadow hover:translate-x-boxShadowX hover:translate-y-boxShadowY hover:shadow-none',
		variant === 'reverse' &&
			'text-main-foreground bg-main border-2 border-border hover:translate-x-reverseBoxShadowX hover:translate-y-reverseBoxShadowY hover:shadow-shadow',
		size === 'default' && 'h-10 px-4 py-2',
		size === 'sm' && 'h-9 px-3',
		size === 'lg' && 'h-11 px-8',
		size === 'icon' && 'size-10',
		className
	]
		.filter(Boolean)
		.join(' ');
</script>

<button {...props} data-slot="button" class={buttonClasses}>
	{@render children()}
</button>
