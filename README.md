Two Asset Bundles made.
More than three presets made and applied.

Code for Making Asset bundle used:
______________________________________________________
using UnityEngine;
using UnityEditor;

public class CreateAssetBundles
{
    [MenuItem("Assets/Create AssetBundles")]
    static void BuildAllAssetBundles()
    {
        // Define the output directory for AssetBundles
        string outputPath = "Assets/AssetBundles";

        // Ensure the output directory exists
        if (!AssetDatabase.IsValidFolder(outputPath))
        {
            AssetDatabase.CreateFolder("Assets", "AssetBundles");
        }

        // Build AssetBundles
        BuildPipeline.BuildAssetBundles(outputPath, BuildAssetBundleOptions.None, BuildTarget.StandaloneWindows);
    }
}

______________________________________________________
