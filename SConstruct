import sys
sys.path.append(Dir('#/scons_site').abspath)
import test1

env = Environment(O = "#/files")

aaaa = SConscript('src/SConscript', variant_dir = env.subst('$O'),
		  duplicate = 0, exports = 'env')

bbbb = SConscript('bbb/SConscript', exports = 'env')
deps_list = test1.deps_list()
print(deps_list)
env.Depends(bbbb, deps_list)
