# Component Spec: Component

## Component

Button

## Description

Reusable button component with multiple variants, sizes, and states. Built on DESIGN.md tokens.

## Props

- **variant**: {'type': 'enum', 'values': ['primary', 'secondary', 'outline', 'ghost'], 'default': 'primary', 'description': 'Visual style variant'}
- **size**: {'type': 'enum', 'values': ['sm', 'md', 'lg'], 'default': 'md', 'description': 'Button size'}
- **disabled**: {'type': 'boolean', 'default': False, 'description': 'Disables interaction and applies disabled styles'}
- **loading**: {'type': 'boolean', 'default': False, 'description': 'Shows spinner, disables interaction, preserves width'}
- **fullWidth**: {'type': 'boolean', 'default': False, 'description': 'Button expands to container width'}
- **leftIcon**: {'type': 'ReactNode', 'description': 'Icon before label'}
- **rightIcon**: {'type': 'ReactNode', 'description': 'Icon after label'}
- **asChild**: {'type': 'boolean', 'default': False, 'description': 'Render as child element (for Link/Router integration)'}
- **type**: {'type': 'enum', 'values': ['button', 'submit', 'reset'], 'default': 'button'}
- **onClick**: {'type': 'function', 'description': 'Click handler'}
- **children**: {'type': 'ReactNode', 'required': True, 'description': 'Button label/content'}
- **className**: {'type': 'string', 'description': 'Additional CSS classes'}
- **aria-label**: {'type': 'string', 'description': 'Accessible label when children is icon-only'}
- **aria-describedby**: {'type': 'string', 'description': 'References element describing button'}

## Variants

- **primary**: {'base': {'backgroundColor': 'color.primary.600', 'color': 'color.text.inverse', 'border': 'none', 'boxShadow': 'shadow.card'}, 'hover': {'backgroundColor': 'color.primary.700', 'boxShadow': 'shadow.lg'}, 'active': {'backgroundColor': 'color.primary.800', 'boxShadow': 'shadow.sm'}, 'focus': {'boxShadow': 'shadow.focus, shadow.card'}, 'disabled': {'backgroundColor': 'color.neutral.300', 'color': 'color.neutral.500', 'boxShadow': 'none', 'cursor': 'not-allowed'}, 'loading': {'backgroundColor': 'color.primary.600', 'color': 'transparent'}}
- **secondary**: {'base': {'backgroundColor': 'color.secondary.600', 'color': 'color.text.inverse', 'border': 'none', 'boxShadow': 'shadow.card'}, 'hover': {'backgroundColor': 'color.secondary.700', 'boxShadow': 'shadow.lg'}, 'active': {'backgroundColor': 'color.secondary.800', 'boxShadow': 'shadow.sm'}, 'focus': {'boxShadow': 'shadow.focus, shadow.card'}, 'disabled': {'backgroundColor': 'color.neutral.300', 'color': 'color.neutral.500', 'boxShadow': 'none', 'cursor': 'not-allowed'}}
- **outline**: {'base': {'backgroundColor': 'transparent', 'color': 'color.primary.600', 'border': '2px solid', 'borderColor': 'color.primary.600', 'boxShadow': 'none'}, 'hover': {'backgroundColor': 'color.primary.50', 'color': 'color.primary.700', 'borderColor': 'color.primary.700'}, 'active': {'backgroundColor': 'color.primary.100', 'color': 'color.primary.800', 'borderColor': 'color.primary.800'}, 'focus': {'boxShadow': 'shadow.focus'}, 'disabled': {'color': 'color.neutral.400', 'borderColor': 'color.neutral.300', 'cursor': 'not-allowed'}}
- **ghost**: {'base': {'backgroundColor': 'transparent', 'color': 'color.text.primary', 'border': 'none', 'boxShadow': 'none'}, 'hover': {'backgroundColor': 'color.neutral.100', 'color': 'color.text.primary'}, 'active': {'backgroundColor': 'color.neutral.200'}, 'focus': {'boxShadow': 'shadow.focus'}, 'disabled': {'color': 'color.neutral.400', 'cursor': 'not-allowed'}}

## Sizes

- **sm**: {'height': '2rem', 'paddingX': 'space.3', 'fontSize': 'typography.fontSize.sm', 'fontWeight': 'typography.fontWeight.medium', 'gap': 'space.1.5', 'borderRadius': 'radius.md', 'iconSize': '1rem'}
- **md**: {'height': '2.75rem', 'paddingX': 'space.5', 'fontSize': 'typography.fontSize.base', 'fontWeight': 'typography.fontWeight.medium', 'gap': 'space.2', 'borderRadius': 'radius.lg', 'iconSize': '1.125rem'}
- **lg**: {'height': '3.5rem', 'paddingX': 'space.7', 'fontSize': 'typography.fontSize.lg', 'fontWeight': 'typography.fontWeight.semibold', 'gap': 'space.2.5', 'borderRadius': 'radius.xl', 'iconSize': '1.25rem'}

## States

- **default**: Base styles per variant/size
- **hover**: Applied on mouse hover (not touch)
- **active**: Applied on mousedown/keyboard press
- **focus**: Applied on keyboard focus (visible ring)
- **focusVisible**: Focus ring only when keyboard navigation detected
- **disabled**: Non-interactive, reduced opacity, not-allowed cursor
- **loading**: Spinner replaces content, width preserved, pointer-events none

## Accessibility

- **keyboard**: {'tabIndex': 0, 'enter': 'Activates onClick', 'space': 'Activates onClick', 'focusRing': '3px solid color.primary.500 / 35% (shadow.focus token)'}
- **screenReader**: {'role': 'button', 'ariaDisabled': 'true when disabled prop', 'ariaBusy': 'true when loading prop', 'ariaLabel': 'Required when children is icon-only', 'ariaDescribedBy': 'Optional reference to descriptive text'}
- **colorContrast**: {'primary': 'AA on white (primary.600 #EA580C)', 'secondary': 'AA on white (secondary.600 #059669)', 'outline': 'AA text on white (primary.600)', 'ghost': 'AA text on white (neutral.900)'}
- **reducedMotion**: {'respectsPrefersReducedMotion': True, 'animationDisabled': 'All transitions disabled when prefers-reduced-motion: reduce'}

## Usageexamples

- {'name': 'Primary CTA', 'code': '<Button variant="primary" size="lg">Start Free Trial</Button>', 'description': 'Main call-to-action, hero sections'}
- {'name': 'Secondary Action', 'code': '<Button variant="secondary">Save Changes</Button>', 'description': 'Confirm/success actions (orders, bookings)'}
- {'name': 'Outline Button', 'code': '<Button variant="outline">View Menu</Button>', 'description': 'Secondary actions on colored backgrounds'}
- {'name': 'Ghost Button', 'code': '<Button variant="ghost" size="sm">Cancel</Button>', 'description': 'Tertiary actions, inline with content'}
- {'name': 'Loading State', 'code': '<Button variant="primary" loading>Processing...</Button>', 'description': 'Async operations, form submissions'}
- {'name': 'With Icons', 'code': '<Button variant="primary" leftIcon={<ShoppingCart />} rightIcon={<ArrowRight />}>Add to Cart</Button>', 'description': 'Icon + label combinations'}
- {'name': 'Icon Only', 'code': '<Button variant="ghost" size="sm" aria-label="Delete item"><TrashIcon /></Button>', 'description': 'Toolbar actions, requires aria-label'}
- {'name': 'As Link', 'code': '<Button asChild><Link href="/menu">View Menu</Link></Button>', 'description': 'Router/Link integration via asChild'}
- {'name': 'Full Width Mobile', 'code': '<Button variant="primary" fullWidth className="lg:fullWidth-false">Book Table</Button>', 'description': 'Responsive full-width on mobile'}
