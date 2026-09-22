# Construction Material Embodied Carbon API

I need the embodied carbon of a construction material in kg CO2e to compare building options. Buildings are chosen on operational energy, but embodied carbon in materials is often a large share of lifetime impact and is rarely compared.

Construction Material Embodied Carbon API returns an embodied carbon figure for a construction material. A call to GET /materials/{id} returns { "kgCO2ePerKg": 1.1, "unit": "kg", "source": "reference dataset 2024" }.

Limits: figures come from generic reference datasets and vary by supplier, transport and process. Results are indicative and not a certified assessment.

Status: pre-launch. The endpoints described here are not yet live; request early access from the link on this page.

The source field names the reference dataset a figure came from so different datasets can be compared transparently. No single figure can stand in for a project-specific assessment.

A typical caller is a designer comparing material options early in a project. The figure is meant for relative comparison rather than for a formal lifecycle assessment.

The unit is made explicit so figures for materials reported in different units are not silently mixed.
