# Copyright (c) 2012, 2018, Codership Oy. All rights reserved.
# 
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; version 2 of the License.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301 USA

SET(WSREP_SOURCES src/wsrep_gtid.c src/wsrep_uuid.c src/wsrep_loader.c src/wsrep_dummy.c)

ADD_CONVENIENCE_LIBRARY(wsrep ${WSREP_SOURCES})
DTRACE_INSTRUMENT(wsrep)

#ADD_EXECUTABLE(listener wsrep_listener.c ${WSREP_SOURCES})
#TARGET_LINK_LIBRARIES(listener ${LIBDL})
