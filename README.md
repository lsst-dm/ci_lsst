You need the raw data; it's currently [here](https://github.com/lsst-dm/testdata_obs_lsst).

To run the complete test suite, say

    run_ci_lsst_pipeline --raw $TESTDATA_OBS_LSST_DIR/raws --dir [path_to_work_dir]

Where you can optionally specify a list of cameras.

This is equivalent to

    ingest_ci_lsst --raw $TESTDATA_OBS_LSST_DIR/raws --dir [path_to_work_dir]
    createCalibs_ci_lsst
    runIsr_ci_lsst
    processCcd_ci_lsst
