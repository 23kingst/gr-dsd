# Copyright 2012 Clayton Smith
#
# This file is part of gr-dsd
#
# gr-dsd is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 3, or (at your option)
# any later version.
#
# gr-dsd is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with gr-dsd; see the file COPYING.  If not, write to
# the Free Software Foundation, Inc., 51 Franklin Street,
# Boston, MA 02110-1301, USA.

#include(git_revision)
#git_describe(GIT_TAG)

set(CMAKE_BUILD_TYPE Debug)

add_library(dsd dmr_data.c dmr_voice.c dsd_audio.c dsd_dibit.c dsd_file.c dsd_frame.c dsd_frame_sync.c dsd_main.c dsd_mbe.c dsd_serial.c dsd_filters.c dsd_symbol.c dsd_upsample.c dstar.c dstar_header.c Hamming.cpp nxdn96.c nxdn_data.c nxdn_voice.c p25_lcw.c p25p1_check_hdu.cpp p25p1_heuristics.c p25p1_tdu.c p25p1_check_nid.cpp p25p1_check_ldu.cpp p25p1_hdu.c p25p1_ldu1.c p25p1_ldu2.c p25p1_ldu.c p25p1_tdulc.c provoice.c x2tdma_data.c x2tdma_voice.c)
target_link_libraries(dsd mbe sndfile)
add_definitions(-fPIC)
