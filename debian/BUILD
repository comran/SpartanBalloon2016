package(default_visibility = ['//visibility:public'])

load('/tools/build_rules/select', 'cpu_select')

[ cc_library(
  name = libname,
  deps = cpu_select({
    "amd64": ['@usr_repo//:' + libname],
    "raspi": ['@gcc_linaro_arm_linux_gnueabihf_raspbian_repo//:' + libname],
  }),
) for libname in ['libpthread', 'libm', 'libdl', 'librt']]
