# clone the package you want to develop in the same folder as scratch-gui
# (folder doesn't really matter but it makes things easier to keep track of)
cd scratch-gui/..
git clone https://github.com/TurboWarp/scratch-vm

# install dependencies in the child package
cd scratch-vm
npm ci

# tell npm that this is your local copy of the package
npm link

# for some packages (eg. storage, svg-renderer), you may need to build for your changes to apply
npm run build

# tell scratch-gui to use your local copy of the package
cd ../scratch-gui
npm link scratch-vm
