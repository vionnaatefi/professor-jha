# professor-jha
persee.fr data extraction and processing files

00: persee_extracted_data.xlsx (All OCRs downloaded from the persee.fr website (OCRs included in the page_text field))

01: merged_data.xlsx (Persee data merged with hyslop_dummies_new_dict.xlsx on the bailliage column)

02: unmatched_data.xlsx (Persee data that didn't find a match on a baillage column of hyslop_dummies_new_dict.xlsx)

03: filtered_merged_data.xlsx (Filter out all columns that presumably come from a paroisse rather than a baillage)


Overview of data processing (persse_extracted_data.xlsx => filtered_nerged_data.xlsx):

•	All available OCRs of Cahiers de Doleances were manually downloaded from the persee.fr website (link: https://archives-parlementaires.persee.fr/explorer/les-cahiers-de-doleances?page=0)

•	From the document names of the cahiers, as labeled on the persee.fr website, both the document état and the cahier location (paroisse or baillage name) were extracted and included as data fields.

•	Location names were cross referenced with Victor Gay’s encoding of baillage names from the hyslop_dummies_new_dict.xlsx spreadsheet created by Saumitra Jha. Where a location field from the persee OCRs matched a baillage name according to the Gay encoding, the cahier was included in merged_data.xlsx. Where matches didn’t exist, cahiers were included in unmatch_persee_data.xlsx. 

•	filtered_merged_data.xlsx further pulls out cahiers corresponding to paroisses and endeavors to include one data row for each baillage / état pair. 
o	Where three cahiers per baillage are not available, hypothetically the hyslop_dummies_new_dict.xlsx spreadsheet should indicate a missing cahier for that baillage / cahier pair. Where a “missing” data entry doesn’t correspond to a missing entry in the filtered_merged_data.xlsx spreadsheet, this corresponds to a hypothetically missing cahier from the persee.fr website that still needs to be tracked down and added as a data row. 


