project(k2pdfopt C)
cmake_minimum_required(VERSION 2.6)

include_directories(..)

set(WILLUSLIB_SRC
        ansi.c array.c bmp.c dtcompress.c filelist.c
        fontdata.c fontrender.c gslpolyfit.c linux.c math.c mem.c ocr.c
        ocrgocr.c ocrtess.c pdfwrite.c point2d.c render.c strbuf.c string.c
        token.c wfile.c wgs.c wgui.c willusversion.c winbmp.c win.c wincomdlg.c
        winmbox.c winshell.c winshellwapi.c wleptonica.c wmupdfinfo.c
        wpdf.c wsys.c wzfile.c
        )

if (DJVU_FOUND)
    set(WILLUSLIB_SRC ${WILLUSLIB_SRC} bmpdjvu.c)
endif (DJVU_FOUND)

if (MUPDF_FOUND)
    set(WILLUSLIB_SRC ${WILLUSLIB_SRC} bmpmupdf.c wmupdf.c)
endif (MUPDF_FOUND)

message("-- Willuslib sources: ${WILLUSLIB_SRC}")

add_library(willuslib ${WILLUSLIB_SRC})

# HAVE_GOCR_LIB: ocrjocr.c
# HAVE_TESSERACT_LIB: ocrtess.c 

