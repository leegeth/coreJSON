# Copyright Amazon.com, Inc. or its affiliates. All Rights Reserved.
# SPDX-License-Identifier: Apache-2.0

HARNESS_FILE=skipUTF8_harness

# This value was experimentally chosen to provide 100% coverage
# without tripping unwinding assertions and without exhausting memory.
CBMC_MAX_BUFSIZE=10

UNWINDSET += countHighBits.0:9
UNWINDSET += skipUTF8.0:$(CBMC_MAX_BUFSIZE)
UNWINDSET += skipUTF8MultiByte.0:$(CBMC_MAX_BUFSIZE)

include ../Makefile-json.common

$(PROOFDIR)/core_json.c: $(SRCDIR)/source/core_json.c
	sed 's/^static //' $< > $@
