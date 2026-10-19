This dataset supports research on AI model adoption and diffusion across protein research fields during 2020–2025. It contains citation records with citing and cited DOIs, citation-intent labels (Background, Tool, and Method), publication dates, research-field assignments, and disciplinary subject attributes. Supporting tables provide cited-model metadata, mappings for ten research hotspots, and five model categories.

The dataset also includes a publication sampling frame, a field-by-year Top50 high-citation sample, and publication-level innovation-output annotations. These files support analyses of citation-intent distributions, model coverage and diversity, temporal adoption patterns, cross-disciplinary differences, and innovation-output structures. File contents and fields are documented in the accompanying README and data dictionary.

Owing to space limitations in the main article, the complete MDE calculation process could not be included in the appendix. The full calculation — per-hotspot model citation frequencies, exact shares, individual entropy contributions, and the worked formula for each of the ten hotspots — is provided in `MDE Calculation Process (CompleteVersion).md`.

# Data files and fields

| File | Contents | Fields |
|---|---|---|
| `citation_records.csv` | Citation records with intent, hotspot and subject attributes. | `citation_id`, `source_doi`, `target_doi`, `intent_raw`, `field_name_zh_raw`, `publication_date`, `subject_json_raw`, `publication_year`, `intent`, `field_code`, `in_core_model_analysis` |
| `citation_subject_memberships.csv` | Citation-to-subject memberships. | `membership_id`, `citation_id`, `subject` |
| `cited_model_metadata.csv` | Metadata for cited model publications. | `metadata_id`, `target_doi`, `model_name`, `model_type_zh`, `title`, `publication_year`, `publication_date`, `target_doi_key` |
| `field_mapping.csv` | Hotspot codes and Chinese and English names. | `field_code`, `field_name_zh`, `field_short_en` |
| `model_type_mapping.csv` | Model-category codes and Chinese and English names. | `model_type_code`, `model_type_cn`, `model_type_en`, `model_type_short_en` |
| `innovation_sampling_frame.csv` | Candidate publications and within-field/year ranks for innovation-output analysis. | `publication_key`, `doi`, `title`, `year`, `times_cited`, `area`, `source_row_count`, `area_value_count`, `year_value_count`, `field_code`, `field_year_citation_rank` |
| `innovation_top50_publications.csv` | Field-year Top50 selected publications and sample attributes. | `publication_key`, `doi`, `title`, `year`, `times_cited`, `area`, `field_code`, `field_en`, `group_en`, `field_year_citation_rank`, `source_row_count`, `area_value_count`, `year_value_count`, `selection_rule`, `conclusion_source` |
| `innovation_output_annotations.csv` | Publication-level innovation categories, confidence labels and classification scores. | `publication_key`, `innovation_type_en`, `major_type_en`, `confidence`, `score_computational_method`, `score_tool_resource`, `score_experimental_strategy`, `score_molecular_material_product`, `score_mechanism_theory_insight` |
| `innovation_output_categories.csv` | Mapping between primary and broader innovation-output categories. | `innovation_type_en`, `major_type_en` |
| `data_dictionary.csv` | Data-column definitions. | `file`, `column`, `description`, `missing_value` |
| `file_inventory.csv` | Data filenames, row counts and purposes. | `file`, `rows`, `purpose` |
| `validation_checks.csv` | Data-check names, statuses and details. | `check`, `status`, `details` |
| `checksums.csv` | File sizes and SHA-256 checksums. | `file`, `bytes`, `sha256` |
| `MDE Calculation Process (CompleteVersion).md` | Complete calculation record for the model-diversity entropy (MDE) of the ten core hotspots (F01–F10): per-hotspot model citation frequencies, exact shares, individual entropy contributions, worked MDE formulas, and a summary table. Documentation only, not a data table. | Not applicable |

