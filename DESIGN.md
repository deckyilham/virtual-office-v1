# Design Tokens

## Color

- `primary`: {'50': '#FFF7ED', '100': '#FFEDD5', '200': '#FED7AA', '300': '#FDBA74', '400': '#FB923C', '500': '#F97316', '600': '#EA580C', '700': '#C2410C', '800': '#9A3412', '900': '#7C2D12'}
- `secondary`: {'50': '#ECFDF5', '100': '#D1FAE5', '200': '#A7F3D0', '300': '#6EE7B7', '400': '#34D399', '500': '#10B981', '600': '#059669', '700': '#047857', '800': '#065F46', '900': '#064E3B'}
- `neutral`: {'0': '#FFFFFF', '50': '#FAFAF9', '100': '#F5F5F4', '200': '#E7E5E4', '300': '#D6D3D1', '400': '#A8A29E', '500': '#78716C', '600': '#57534E', '700': '#44403C', '800': '#292524', '900': '#1C1917', '1000': '#0C0A09'}
- `semantic`: {'success': '#10B981', 'warning': '#F59E0B', 'error': '#EF4444', 'info': '#3B82F6', 'successBg': '#ECFDF5', 'warningBg': '#FFFBEB', 'errorBg': '#FEF2F2', 'infoBg': '#EFF6FF'}
- `text`: {'primary': '#1C1917', 'secondary': '#57534E', 'tertiary': '#A8A29E', 'inverse': '#FAFAF9', 'link': '#EA580C'}
- `surface`: {'base': '#FFFFFF', 'subtle': '#FAFAF9', 'muted': '#F5F5F4', 'inverse': '#1C1917'}
- `border`: {'default': '#E7E5E4', 'strong': '#D6D3D1', 'focus': '#F97316'}

## Typography

- `fontFamily`: {'sans': "'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif", 'display': "'Plus Jakarta Sans', 'Inter', sans-serif", 'mono': "'JetBrains Mono', ui-monospace, monospace"}
- `fontSize`: {'xs': '0.75rem', 'sm': '0.875rem', 'base': '1rem', 'lg': '1.125rem', 'xl': '1.25rem', '2xl': '1.5rem', '3xl': '1.875rem', '4xl': '2.25rem', '5xl': '3rem', '6xl': '3.75rem', '7xl': '4.5rem'}
- `fontWeight`: {'regular': 400, 'medium': 500, 'semibold': 600, 'bold': 700, 'extrabold': 800}
- `lineHeight`: {'none': '1', 'tight': '1.15', 'snug': '1.3', 'normal': '1.5', 'relaxed': '1.65', 'loose': '2'}
- `letterSpacing`: {'tighter': '-0.03em', 'tight': '-0.02em', 'normal': '0', 'wide': '0.02em', 'wider': '0.05em'}
- `textStyle`: {'display': {'fontSize': '4.5rem', 'lineHeight': '1.05', 'fontWeight': 800, 'letterSpacing': '-0.03em'}, 'h1': {'fontSize': '3rem', 'lineHeight': '1.15', 'fontWeight': 700, 'letterSpacing': '-0.02em'}, 'h2': {'fontSize': '2.25rem', 'lineHeight': '1.2', 'fontWeight': 700, 'letterSpacing': '-0.02em'}, 'h3': {'fontSize': '1.875rem', 'lineHeight': '1.3', 'fontWeight': 600, 'letterSpacing': '-0.01em'}, 'h4': {'fontSize': '1.5rem', 'lineHeight': '1.35', 'fontWeight': 600}, 'bodyLg': {'fontSize': '1.125rem', 'lineHeight': '1.65', 'fontWeight': 400}, 'body': {'fontSize': '1rem', 'lineHeight': '1.5', 'fontWeight': 400}, 'bodySm': {'fontSize': '0.875rem', 'lineHeight': '1.5', 'fontWeight': 400}, 'label': {'fontSize': '0.875rem', 'lineHeight': '1.3', 'fontWeight': 500}, 'caption': {'fontSize': '0.75rem', 'lineHeight': '1.4', 'fontWeight': 500, 'letterSpacing': '0.02em'}}

## Space

- `0`: 0
- `1`: 0.25rem
- `2`: 0.5rem
- `3`: 0.75rem
- `4`: 1rem
- `5`: 1.25rem
- `6`: 1.5rem
- `8`: 2rem
- `10`: 2.5rem
- `12`: 3rem
- `16`: 4rem
- `20`: 5rem
- `24`: 6rem
- `32`: 8rem
- `40`: 10rem

## Radius

- `none`: 0
- `sm`: 0.375rem
- `md`: 0.5rem
- `lg`: 0.75rem
- `xl`: 1rem
- `2xl`: 1.5rem
- `3xl`: 2rem
- `full`: 9999px

## Shadow

- `xs`: 0 1px 2px 0 rgb(28 25 23 / 0.05)
- `sm`: 0 1px 3px 0 rgb(28 25 23 / 0.08), 0 1px 2px -1px rgb(28 25 23 / 0.06)
- `md`: 0 4px 6px -1px rgb(28 25 23 / 0.08), 0 2px 4px -2px rgb(28 25 23 / 0.06)
- `lg`: 0 10px 15px -3px rgb(28 25 23 / 0.08), 0 4px 6px -4px rgb(28 25 23 / 0.05)
- `xl`: 0 20px 25px -5px rgb(28 25 23 / 0.10), 0 8px 10px -6px rgb(28 25 23 / 0.05)
- `2xl`: 0 25px 50px -12px rgb(28 25 23 / 0.20)
- `card`: 0 2px 8px -2px rgb(28 25 23 / 0.06), 0 4px 16px -4px rgb(28 25 23 / 0.08)
- `focus`: 0 0 0 3px rgb(249 115 22 / 0.35)

## Breakpoint

- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px
- `2xl`: 1536px

## Zindex

- `base`: 0
- `raised`: 10
- `dropdown`: 1000
- `sticky`: 1100
- `overlay`: 1200
- `modal`: 1300
- `toast`: 1400
- `tooltip`: 1500

## Motion

- `duration`: {'fast': '150ms', 'base': '250ms', 'slow': '400ms'}
- `easing`: {'out': 'cubic-bezier(0.16, 1, 0.3, 1)', 'inOut': 'cubic-bezier(0.4, 0, 0.2, 1)'}
