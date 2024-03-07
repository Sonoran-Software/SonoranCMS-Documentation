# Troubleshooting

### CMS Not Loading (ESET Antivirus)

In certain cases, antivirus programs such as ESET are known to block connections to the CMS. To add CMS to ESET's allow list, please follow the following instructions:

1. Open ESET program on your computer
2. Press the `F5` key to open Advanced setup.
3. Click `Web access protection`. Expand `URL list management` and click `Edit` next to `Address list`
4. Select `List of allowed addresses` and click `Edit`
5. Click `Add` in the `Edit list` window. Paste `*sonorancms.com*` in the respective field, click `OK` → `OK` to save your changes, and exit the Advanced setup window.
   * If using CAD, also add `*.sonorancad.com*`

For more information, see [here](https://support.eset.com/en/kb2960-exclude-a-safe-website-from-being-blocked-by-web-access-protection).
