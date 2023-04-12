# Essential assets

Adds an object to the tender and lot objects to describe the assets used for the provision of public services.

If you are using the [Lots extension](https://extensions.open-contracting.org/en/extensions/lots/master/), [follow its guidance](https://extensions.open-contracting.org/en/extensions/lots/master/#usage) on whether to use `tender.lots` fields or `tender` fields.

## Legal context

In the European Union, this extension's fields correspond to [eForms OPT-020-Contract (Assets related contract extension indicator), OPT-021-Contract (Used asset), OPT-022-Contract (Significance (%)), and OPT-023-Contract (Precominance (%))](https://docs.ted.europa.eu/eforms/latest/reference/business-terms/). For correspondences to eForms fields, see [OCDS for eForms](https://standard.open-contracting.org/profiles/eforms/).

## Examples

### Tender

```json
{
  "tender": {
    "hasEssentialAssets": true,
    "essentialAssets": {
      "description": "Significant investments have been made by the supplier in the past years and will continue to be so in the future, which will pay for themselves over a period of time well beyond the period of the contract. It includes the purchase of new vehicles, the maintenance of the modernization of the existing fleet and the renovation of the vehicle depots.",
      "significance": "30",
      "predominance": "40"
    }
  }
}
```

### Lot

```json
{
  "tender": {
    "lots": [
      {
        "id": "LOT-0001",
        "hasEssentialAssets": true,
        "essentialAssets": {
          "description": "Significant investments have been made by the supplier in the past years and will continue to be so in the future, which will pay for themselves over a period of time well beyond the period of the contract. It includes the purchase of new vehicles, the maintenance of the modernization of the existing fleet and the renovation of the vehicle depots.",
          "significance": "30",
          "predominance": "40"
        }
      }
    ]
  }
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.

## Changelog

### 2023-04-05

* Add `essentialAssets` and `hasEssentialAssets` to the `Lot` object.

### 2020-04-24

* Add `minProperties`, `minItems` and/or `minLength` properties.

This extension was originally discussed as part of the OCDS for EU profile in [issue #60](https://github.com/open-contracting-extensions/european-union/issues/60) and in [pull requests](https://github.com/open-contracting-extensions/ocds_essentialAssets_extension/pulls?q=is%3Apr+is%3Aclosed).
