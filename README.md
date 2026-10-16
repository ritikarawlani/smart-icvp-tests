# smart-icvp-tests

The conformance **Test Plan** and test cases for the **ICVP** (International Certificate of Vaccination or Prophylaxis) in the **digital format**. They run on the [WHO-ITB](https://github.com/WorldHealthOrganization/WHO-ITB) and test against the [smart-icvp](https://github.com/WorldHealthOrganization/smart-icvp) payload.

> **Status:** not started. The scope, decisions and candidate requirements are tracked in
> [litlfred/folio-assistant#2601](https://github.com/litlfred/folio-assistant/issues/2601).

## Scope

- **One Test Plan**: a single FHIR `TestPlan` with every ICVP test case under it.
- **Gherkin is mandatory**: every test case is authored as an [OTB Gherkin](https://github.com/OpenTestBed/itb-plugin-authoring) feature and compiled to GITB TDL.
- **Source of criteria**: the WHO technical guidance on the amended Model ICVP (IHR (2005), Annex 6, as amended through WHA77.17 (2024)).
- **Payload**: smart-icvp is authoritative for elements, cardinalities and value-set bindings.
- **Digital format only**: paper certificates are out of scope.

## Toolchain

Built on [OpenTestBed](https://github.com/OpenTestBed):
[itb-plugin-authoring](https://github.com/OpenTestBed/itb-plugin-authoring) (Gherkin → TDL, test IG packaging),
[itb-plugin-hcert-decoder](https://github.com/OpenTestBed/itb-plugin-hcert-decoder),
[itb-plugin-fhir-validator](https://github.com/OpenTestBed/itb-plugin-fhir-validator),
[itb-plugin-jwt](https://github.com/OpenTestBed/itb-plugin-jwt) and
[itb-cli](https://github.com/OpenTestBed/itb-cli).
