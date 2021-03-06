# Copyright 2016 The Closure Rules Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

package(default_visibility = ["//visibility:public"])

licenses(["notice"])  # Apache 2.0

load("@rules_java//java:defs.bzl", "java_library")
load("//closure:defs.bzl", "closure_js_library", "closure_js_proto_library")

java_library(
    name = "templates",
    exports = ["@com_google_template_soy"],
)

closure_js_proto_library(
    name = "soy_html_proto",
    srcs = ["@com_google_common_html_types_html_proto//file"],
)

closure_js_library(
    name = "soy_jssrc",
    srcs = ["@com_google_template_soy_jssrc"],
    lenient = True,
    deps = [
        ":soy_html_proto",
        "//closure/library/array",
        "//closure/library/asserts",
        "//closure/library/debug",
        "//closure/library/format",
        "//closure/library/html:safehtml",
        "//closure/library/html:safescript",
        "//closure/library/html:safestyle",
        "//closure/library/html:safestylesheet",
        "//closure/library/html:safeurl",
        "//closure/library/html:trustedresourceurl",
        "//closure/library/html:uncheckedconversions",
        "//closure/library/i18n:bidi",
        "//closure/library/i18n:bidiformatter",
        "//closure/library/i18n:numberformat",
        "//closure/library/object",
        "//closure/library/soy:all_js",
        "//closure/library/string",
        "//closure/library/string:const",
        "//closure/library/uri",
    ],
)

java_library(
    name = "safe_html_types",
    exports = ["@com_google_common_html_types"],
)
