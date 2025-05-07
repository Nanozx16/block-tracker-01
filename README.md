# block-tracker-01
Upgrade to Yarn v4 (#289)
This commit aligns this repo more closely with our module template.

- Add `packageManager` to `package.json`
- Add `allow-scripts` Yarn plugin
- Add Yarn constraints (but modified to suit this package, whose build
pipeline is not fully standardized with the module template)
- Remove `setup` script (since `allow-scripts` gets called automatically
now)
- Replace `prepublishOnly` script with `prepack`
- Update GitHub workflow to install Yarn via Corepack
- Update Yarn-specific section of `.gitignore`
- Update installation instructions in README
- Upgrade `eslint-plugin-jsdoc` as the version we were using was
previously not compatible with the version of Node we are using, but
Yarn v1 did not pick this up. Fix lint violations to match.
