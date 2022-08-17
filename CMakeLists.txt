cmake_minimum_required(VERSION 3.22)
project(mimetic)

set(CMAKE_CXX_STANDARD 17)

include_directories(examples)
include_directories(mimetic)
include_directories(mimetic/codec)
include_directories(mimetic/os)
include_directories(mimetic/parser)
include_directories(mimetic/rfc822)
include_directories(test)

add_library(mimetic SHARED
        mimetic/codec/base64.cxx
        mimetic/codec/base64.h
        mimetic/codec/code.h
        mimetic/codec/codec.h
        mimetic/codec/codec_base.h
        mimetic/codec/codec_chain.h
        mimetic/codec/other_codecs.h
        mimetic/codec/qp.cxx
        mimetic/codec/qp.h
        mimetic/os/directory.h
        mimetic/os/file.h
        mimetic/os/file_iterator.cxx
        mimetic/os/file_iterator.h
        mimetic/os/fileop.cxx
        mimetic/os/fileop.h
#        mimetic/os/mmfile.cxx
        mimetic/os/mmfile.h
        mimetic/os/os.h
        mimetic/os/stdfile.cxx
        mimetic/os/stdfile.h
        mimetic/os/utils.cxx
        mimetic/os/utils.h
        mimetic/parser/itparser.h
#        mimetic/parser/itparserdecl.h
        mimetic/rfc822/address.cxx
        mimetic/rfc822/address.h
        mimetic/rfc822/addresslist.cxx
        mimetic/rfc822/addresslist.h
        mimetic/rfc822/body.h
        mimetic/rfc822/datetime.cxx
        mimetic/rfc822/datetime.h
        mimetic/rfc822/field.cxx
        mimetic/rfc822/field.h
        mimetic/rfc822/fieldvalue.cxx
        mimetic/rfc822/fieldvalue.h
        mimetic/rfc822/group.cxx
        mimetic/rfc822/group.h
        mimetic/rfc822/header.cxx
        mimetic/rfc822/header.h
        mimetic/rfc822/mailbox.cxx
        mimetic/rfc822/mailbox.h
        mimetic/rfc822/mailboxlist.cxx
        mimetic/rfc822/mailboxlist.h
        mimetic/rfc822/message.cxx
        mimetic/rfc822/message.h
        mimetic/rfc822/messageid.cxx
        mimetic/rfc822/messageid.h
        mimetic/rfc822/rfc822.h
        mimetic/body.cxx
        mimetic/body.h
        mimetic/circular_buffer.h
        mimetic/config_win32.h
        mimetic/contentdescription.cxx
        mimetic/contentdescription.h
        mimetic/contentdisposition.cxx
        mimetic/contentdisposition.h
        mimetic/contentid.cxx
        mimetic/contentid.h
        mimetic/contenttransferencoding.cxx
        mimetic/contenttransferencoding.h
        mimetic/contenttype.cxx
        mimetic/contenttype.h
        mimetic/fieldparam.cxx
        mimetic/fieldparam.h
        mimetic/header.cxx
        mimetic/header.h
        mimetic/libconfig.h
        mimetic/message.cxx
        mimetic/message.h
        mimetic/mimeentity.cxx
        mimetic/mimeentity.h
        mimetic/mimeentitylist.h
        mimetic/mimetic.h
        mimetic/mimeversion.cxx
        mimetic/mimeversion.h
        mimetic/streambufs.h
        mimetic/strutils.cxx
        mimetic/strutils.h
        mimetic/tokenizer.h
        mimetic/tree.h
        mimetic/utils.cxx
        mimetic/utils.h
        mimetic/version.cxx
        mimetic/version.h)

target_include_directories(mimetic PUBLIC ../ .)
