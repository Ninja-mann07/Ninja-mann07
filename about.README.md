- 👋 Hi, I’m @Ninja-mann07
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
- #!/usr/bin/env bash
set -eu

prefix="/usr/local"

if [ "${PREFIX:-}" != "" ] ; then
  prefix=${PREFIX:-}
elif [ "${BOXEN_HOME:-}" != "" ] ; then
  prefix=${BOXEN_HOME:-}
fi

mkdir -p $prefix/bin
rm -rf $prefix/bin/git-lfs*

pushd "$( dirname "${BASH_SOURCE[0]}" )" > /dev/null
  for g in git*; do
    install $g "$prefix/bin/$g"
  done
popd > /dev/null

PATH+=:$prefix/bin
git lfs install
<!---
Ninja-mann07/Ninja-mann07 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
