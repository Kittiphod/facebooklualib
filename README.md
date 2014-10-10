facebooklualib
By Kittiphod Zhikumano
==============

Skip to content
 This repository
Explore
Gist
Blog
Help
Kittiphod Kittiphod
 
You don't have any verified emails. We recommend verifying at least one email.
Email verification helps our support team verify ownership if you lose account access and allows you to receive all the notifications you ask for.
27  Watch 
  Star 119
 Fork 17facebook/fblualib
 branch: master  fblualib / fblualib / debugger / rockspec / fbdebugger-0.1-1.rockspec
tudortudor on 12 Jul FBLuaLib: initial commit
1 contributor
46 lines (44 sloc)  1.283 kb RawBlameHistory   
--
--  Copyright (c) 2014, Facebook, Inc.
--  All rights reserved.
--
--  This source code is licensed under the BSD-style license found in the
--  LICENSE file in the root directory of this source tree. An additional grant
--  of patent rights can be found in the PATENTS file in the same directory.
--

package = 'fbdebugger'
version = '0.1-1'
source = {
    url = 'https://github.com/facebook/fblualib',
}
description = {
    summary = 'FB Lua Debugger',
    detailed = [[
      This is a general-purpose debugger for Lua. Its command syntax is
      inspired by gdb, and it has special support for printing Torch tensors
      (but Torch is not required). Requires LuaJIT 2.0+.
    ]],
    homepage = 'https://github.com/facebook/fblualib',
    license = 'BSD',
}
supported_platforms = {
    'unix',
}
dependencies = {
    'fbutil >= 0.1',
    'fbeditline >= 0.1',
    'penlight >= 1.3.1',
}
source = {
    url = 'https://github.com/facebook/fblualib',
    dir = 'fblualib/debugger',
}
build = {
    type = 'builtin',
    modules = {
        ['fb.debugger.breakpoint'] = 'fb/debugger/breakpoint.lua',
        ['fb.debugger.init'] = 'fb/debugger/init.lua',
        ['fb.debugger.types'] = 'fb/debugger/types.lua',
        ['fb.debugger.utils'] = 'fb/debugger/utils.lua',
    },
}
Status API Training Shop Blog About
© 2014 GitHub, Inc. Terms Privacy Security Contact
