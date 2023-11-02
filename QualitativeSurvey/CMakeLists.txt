cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(QualitativeSurvey)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/QualitativeSurvey")
set(EXTENSION_CATEGORY "Training")
set(EXTENSION_CONTRIBUTORS "Felix Benter (The University of Sydney)")
set(EXTENSION_DESCRIPTION "This is an example of a simple extension")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/QualitativeSurvey.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/QualitativeSurvey/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(SurveyLoader)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})