# NSP Passport Size Photo Maker – Windows EXE build package

This package wraps the current Phase 3 HTML prototype in Electron and includes a GitHub Actions workflow that builds a Windows x64 NSIS installer.

## Create the EXE without writing code

1. Sign in to GitHub and create a **new private repository** named `nsp-passport-photo-maker`.
2. Upload the contents of this ZIP (not the ZIP itself) to the repository. Make sure `.github/workflows/build-windows.yml` is included.
3. Open the repository's **Actions** tab.
4. Select **Build NSP Windows EXE** and click **Run workflow** (or push/commit the files to `main`).
5. Wait for the workflow to finish successfully.
6. Open the completed workflow run. Under **Artifacts**, download `NSP-Passport-Photo-Maker-Windows-Installer`.
7. Extract the downloaded artifact ZIP. It contains the `.exe` installer.

## Important current limitations

- This is an Electron packaging of the current Phase 3 browser prototype, not yet the finished commercial photo studio product.
- The prototype's simple background color-key tool is not AI background segmentation.
- AI clothes replacement is a UI placeholder and needs a real AI model/service.
- The activation screen is a design preview only. It does not validate license keys or enforce hardware locking.
- The current HTML prototype's photo editing/printing features are basic. Validate print dimensions and DPI with your printer before commercial use.
- A production license system needs a separate protected admin signing tool and public-key verification in the customer app. Do not distribute any private signing key.
- Windows may show an unknown-publisher warning until the installer is code-signed with a trusted certificate.

The GitHub Actions workflow uses a Windows runner to produce the actual Windows installer. No local coding is needed, but uploading the files and starting the workflow are required.
