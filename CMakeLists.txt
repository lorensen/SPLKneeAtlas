cmake_minimum_required(VERSION 2.8)
 
project(SPLKneeAtlas)

configure_file(${SPLKneeAtlas_SOURCE_DIR}/SPLKneeAtlas.config.in  ${SPLKneeAtlas_BINARY_DIR}/SPLKneeAtlas.config @ONLY)

set(ATLAS_NAME SPLKneeAtlas)
set(ATLAS_VOLUME ${SPLKneeAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}Volume.nrrd)
set(ATLAS_VOLUME_NAME ${ATLAS_NAME}Volume)
set(ATLAS_COLOR_TABLE ${SPLKneeAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}Colors.ctbl)
set(ATLAS_COLOR_TABLE_NAME ${ATLAS_NAME}Colors)
set(ATLAS_LABELS ${SPLKneeAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}Labels.nrrd)
set(ATLAS_LABELS_NAME ${ATLAS_NAME}Labels)
set(MRML_FILENAME ${SPLKneeAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${SPLKneeAtlas_SOURCE_DIR}/Atlas/SPLKneeAtlas.mrml.in  ${SPLKneeAtlas_BINARY_DIR}/SPLKneeAtlas.mrml @ONLY)
