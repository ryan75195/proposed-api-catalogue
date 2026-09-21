# Menu Nutrition Annotation

Caterers must show nutrition but often have dishes built from recipes they cannot easily annotate. Manual lookup per ingredient is slow and inconsistent.

Menu Nutrition Annotation estimates nutrition for a dish from its ingredients and portion size. A call to POST /dishes/annotate with { "ingredients": [{ "name": "chickpea", "grams": 200 }] } returns { "kcal": 312, "proteinG": 12, "allergens": [] }.

Limits: estimates are from reference tables and are not lab-verified; results can vary with preparation and brand, and this is not medical advice.

This is a proposed design and is not implemented.

Estimates use reference nutrient tables for generic ingredients, so branded or prepared items can differ materially. Allergen flags are only as reliable as the ingredient list provided.

A typical caller is a canteen or restaurant adding nutrition labels to a digital menu. Estimates are a starting point that a qualified reviewer should confirm before publishing.

Portion size is taken from the recipe so a plate served with a different amount will not match the label.
