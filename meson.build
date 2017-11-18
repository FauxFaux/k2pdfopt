project('k2pdfopt', 'c')

cc = meson.get_compiler('c')

math = cc.find_library('m', required: false)
jbig2dec = cc.find_library('jbig2dec')
jpeg = cc.find_library('jpeg')


dependencies = [
    math,
    dependency('threads'),

    jbig2dec,
    jpeg,

    dependency('freetype2'),
    dependency('harfbuzz'),
    dependency('ddjvuapi'),
    dependency('mupdf'),
    dependency('libpng'),
    dependency('libopenjp2'),
    dependency('zlib'),
]

lib_includes = include_directories(
    'k2pdfoptlib',
    'willuslib'
    )

all_sources = [
    'k2pdfopt.c',
    'k2pdfoptlib/bmpregion.c',
    'k2pdfoptlib/devprofile.c',
    'k2pdfoptlib/k2bmp.c',
    'k2pdfoptlib/k2file.c',
    'k2pdfoptlib/k2files.c',
    'k2pdfoptlib/k2gui.c',
    'k2pdfoptlib/k2gui_cbox.c',
    'k2pdfoptlib/k2gui_osdep.c',
    'k2pdfoptlib/k2gui_overlay.c',
    'k2pdfoptlib/k2mark.c',
    'k2pdfoptlib/k2master.c',
    'k2pdfoptlib/k2mem.c',
    'k2pdfoptlib/k2menu.c',
    'k2pdfoptlib/k2ocr.c',
    'k2pdfoptlib/k2parsecmd.c',
    'k2pdfoptlib/k2proc.c',
    'k2pdfoptlib/k2publish.c',
    'k2pdfoptlib/k2settings2cmd.c',
    'k2pdfoptlib/k2settings.c',
    'k2pdfoptlib/k2sys.c',
    'k2pdfoptlib/k2usage.c',
    'k2pdfoptlib/k2version.c',
    'k2pdfoptlib/pagelist.c',
    'k2pdfoptlib/pageregions.c',
    'k2pdfoptlib/textrows.c',
    'k2pdfoptlib/textwords.c',
    'k2pdfoptlib/userinput.c',
    'k2pdfoptlib/wrapbmp.c',
    'willuslib/ansi.c',
    'willuslib/array.c',
    'willuslib/bmp.c',
    'willuslib/bmpdjvu.c',
    'willuslib/bmpmupdf.c',
    'willuslib/dtcompress.c',
    'willuslib/filelist.c',
    'willuslib/fontdata.c',
    'willuslib/fontrender.c',
    'willuslib/gslpolyfit.c',
    'willuslib/linux.c',
    'willuslib/math.c',
    'willuslib/mem.c',
    'willuslib/ocr.c',
#        'willuslib/ocrgocr.c',
#        'willuslib/ocrtess.c',
    'willuslib/pdfwrite.c',
    'willuslib/point2d.c',
    'willuslib/render.c',
    'willuslib/strbuf.c',
    'willuslib/string.c',
    'willuslib/token.c',
    'willuslib/wfile.c',
    'willuslib/wgs.c',
    'willuslib/wgui.c',
    'willuslib/willusversion.c',
    'willuslib/winbmp.c',
    'willuslib/win.c',
    'willuslib/wincomdlg.c',
    'willuslib/winmbox.c',
    'willuslib/winshell.c',
    'willuslib/winshellwapi.c',
    'willuslib/wleptonica.c',
    'willuslib/wmupdf.c',
    'willuslib/wmupdfinfo.c',
    'willuslib/wpdf.c',
    'willuslib/wsys.c',
    'willuslib/wzfile.c',
]

executable('k2pdfopt',
    dependencies: dependencies,
    include_directories: lib_includes,
    sources: all_sources,
)

