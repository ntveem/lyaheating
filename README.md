# lyaheating

## Data for thermal evolution

The file [heffs.npy](https://github.com/ntveem/lyaheating/blob/master/heffs.npy) is a 5-dimensional matrix, with dimensions of
n_tks x n_tss x n_tgps x 2 x 4

tks = Kinetic temperatures (K)

      np.logspace(np.log10(0.1), np.log10(100.0), num=175)

tss = Spin temperatures (K)

      np.logspace(np.log10(0.1), np.log10(100.0), num=175)

tgps = Gunn-Peterson optical depths

       np.logspace(4.0, 7.0)

The indices within the last (2 x 4) submatrix stand for (continuum, injected) photons, and (net energy loss efficiency, energy loss efficiency to spins, \tilde{salpha}, effective color temperature (K)).

In practice, one only needs the net energy loss efficiency, \tilde{salpha} and effective color temperature.

The net energy loss efficiency is defined in Eq. (10), and, given a model for the continuum and injected Lyman-alpha fluxes, should be used in the temperature evolution as given by Eq. (18) of our paper at [http://arxiv.org/abs/1804.02406](http://arxiv.org/abs/1804.02406)

The dimensionless Wouthuysen-Field coupling coefficient \tilde{salpha}, and the effective color temperature T_{c,eff} are defined in Hirata C., (2006) [astro-ph/0507102](https://arxiv.org/abs/astro-ph/0507102)

## Caveats

The quantities were computed from the solutions of the Fokker Planck equation, which is not a good description of the diffusion of Lyman-alpha photons at the lowest kinetic temperatures. Hirata (2006) tested the validity of the Fokker Planck equation down to tk = 2 K.
