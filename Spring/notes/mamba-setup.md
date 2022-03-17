# `mamba-setup.md`

## TTS base environment

Assuming `mamba` is installed and initialized on your preferred CLI, first create a new environment by running

```
mamba create -n tts-ds-base
```

in that terminal. Then switch to `tts-ds-base` environment you just created by running

```
mamba activate tts-ds-base
```

Then run

```
mamba install numpy pandas scikit-learn matplotlib seaborn jupyter
```

to add `numpy`, `pandas`, `...`, `jupyter` to your `tts-ds-base` environment.

Finally, run

```
mamba create -n tts-ds --clone tts-ds-base
```

to make a copy of the `tts-ds-base` environment called `tts-ds`. Then we can add additional packages to `tts-ds` while having an environment `tts-ds-base` that should contain the bare essentials for the TTS data science course.
