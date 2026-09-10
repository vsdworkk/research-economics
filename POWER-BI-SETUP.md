# Power BI wireframe setup

Use **HTML Content** by Daniel Marsh-Patrick (regular edition, not lite).

1. In Power BI Desktop, create a new measure and paste the complete contents of `productivity-wireframe.dax`, including the measure name.
2. Add the regular HTML Content visual and put **Productivity Wireframe HTML** in its **Values** field. Leave Granularity empty.
3. Set the report page to custom size **3508 × 2480 px**. Set the visual to X = 0, Y = 0, width = 3508, height = 2480.
4. Turn off the visual title and border, and set any container padding to zero. Use HTML rendering, not Markdown. Leave custom stylesheet and style overrides unset initially.
5. Enable **Allow opening URLs** if you want the ABS source hyperlinks to open. Use Power BI's Fit to page view to see the complete page.

The measure is a **static wireframe snapshot**: it contains the current figures, titles and all chart geometry. It requires no model tables and does not react to filters or refresh its values. Title-automation boxes describe future implementation, not working automation.

The HTML is scoped to its own container and contains no JavaScript or external assets. All three line charts are prebuilt HTML/CSS segments; the 19 industry bars are included directly. The 3508 × 2480 layout is fixed: resizing only the visual will clip it rather than reflow it. Aptos is used where available, with Arial fallback.

Validation: DAX string escaping and exact HTML round-trip checked; generated HTML rendered in a browser with matching chart dimensions and no card overflow. The measure has not been executed inside Power BI Desktop, so in-product rendering and DAX parsing remain to be confirmed there.

The existing documented −0.2% chart versus −0.1% headline rounding discrepancy is preserved. See `design-specification.md` for data sources and calculations.

Official visual documentation: https://html-content.com/docs/visual-editions
