load("@rules_cc//cc:defs.bzl", "objc_library")
load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")

objc_library(
    name = "UrlGetClasses",
    srcs = [
        "UrlGet/AppDelegate.m",
        "UrlGet/UrlGetViewController.m",
        "UrlGet/main.m",
    ],
    hdrs = glob(["UrlGet/*.h"]),
    #deps=["sd"]
)

objc_library(name="all", deps=["//Vendor/Texture:Texture"])

objc_library(name="sd", deps=["//Vendor/SDWebImage:SDWebImage"])

ios_application(
    name = "ddx",
    bundle_id = "cn.xiaochuankeji.zuiyouLite-ih",
    families = [
        "iphone",
    ],
    infoplists = [":UrlGet/UrlGet-Info.plist"],
    launch_storyboard = "UrlGet/UrlGetViewController.xib",
    minimum_os_version = "11.0",
    visibility = ["//visibility:public"],
    deps = [":UrlGetClasses"],
)
