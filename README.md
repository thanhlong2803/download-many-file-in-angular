

# Download File In Angular
Angular - Download many file in angular Example

 - **The project** and **structure** of the example mostly follows the best practice and improve codes.
 - **The project** structure has a folder per feature (Page Home within one button download file) while order share / common code (**services, models, content, components & helpers**) is placed in forder let easy build or hande **Design Pattern**. 
 - The path alias '@' has been configured in the **tsconfig.json and webpack.config.js** the maps to the '/src/app' directory. This allow import to be relative to the '/src/app' folder  by prefixing the import path with '@' removing the need to use long relative paths **like improt '.....'**
 - Now, We are build project structure:


 
![enter image description here](https://lh3.googleusercontent.com/_hlfESWR1VubceKAx6mnC2Id_g-4fnev5yjHR5BhZqus-gwV3ia6jobDhW4Mdeo_2YUkwAc91VmQdaxHSR4vY3CBE2FjZtE0Ig6iBRcgp4oGBWd9QrQqp1NsjrQKalnKuLYlM8R9dMHk9-Biya67uUA1n8FzGP-f8-onq4APLKik0giW-An3P9EzPA9KWY7B-vLVRBQspulsqRyju8Mn6LbDlSosrJgWWsj-nvnac1wgzx5FHDJFLx8VuemWiyufvuWq5LaW8anUnwvVUJYXBM9jWfkYCEWeMaL-IHM1BWGSu5c2kSsirC9Opd31xaUxR8V_-_hPtCLSiifaUk6E2dWTitcPyucaOw-uO4k9U4DQcqsjgBODdXlv9RDW8ip67CFjSD7vvg8TjwjnuAv5FM6tsZccUGN5OHNk_t-nP0ih9FZcBwX3x6tbWUCxr0FYqexq0Pezsp_jLhjR6kAepcGitegzQ00XDlU6BsGVEF_d10yOjuHkI4SUdZkG60abe65UzHNPxFia-uuqTFCobYxRhoHBaVjPFP5LrO7bMdWB8hdTD8iaX17JCP7VZiVAFQkv2Y8aae7cBUSCKZKxl6yALec40j4xMzHOOS1F6JcbwxmGu-CQznekCUHl7KR0ZJQMGjZO0ZxOdY7MoDMAfeaHT0j40u-Ku2t-vWXY1jwd_xQuUtH8Ui7giP2QF_yU4_8BAcAR1B3jGDaGEHJwTaieIFPagMjJ_CEUwtCHwmBs_I01UBd72-AAAGjjEQ=w254-h300-no?authuser=0)

Below is all the tutorial project code along with brief descriptions of each file to explain how it all fits together.
## Alert Component Template and Alert Component ,  AlertService Service
***Path: /src/app/_components/alert.component.html***
The alert component template contains the HTML for displaying the alert message template designed.

![enter image description here](https://lh3.googleusercontent.com/j4NebTrs3aRc8a-jBxAReW8ieJ20A8qcnqkvrOr6C5BjduJCIA89p-WC5ZuBqTqCaBzAFLseAKBhXA3L4tKF0LCaGIf0y25EVrcdzGIuurqmiVqZ87fQSr5nuXiyXRfrYhr1tosN_DEktf0WH0WaN6dPeiXisqumLlGfOxvurlh_nKyMWz4EuJy77x2nbOcbykP_aahRZ-3CDuR14Icv5ahhVrhfapGLBKfDwsv12LDA9EPIulyI-Hz9GngBAMgVcl01zvUIxD7h3K8mG_dMey0Dbh-iQrGofXlSUrId8ETlFMSAXEP4HnRe8-xfJstQUub4syB9X6Ab5OlNa4RxlFLsQKXlafVrujA9PRLNx4wQghNwthSf8Qton2tOgQSdEd6pD60b6HuuklCUKH2WEyR7Qk-1-AcoVqHHbon3hkDw0LQkTzMAkJ5bV7C2ax3Dki6SumF6sf3SsNWcZaMMZuRw5LaRWopjmX3GzfiGg4W7tPa0Id8X5WHp3wxRRBwbjH0quuigljlSYTow8nARIVyj6QoBI_TTMP_OU1GdaGXYIjsOXo3zVsW3cM9jWqvqMZ3rXzUW3aHG3EzVplkf-jkGDoqPo1-VC79fbJX8k8Ha0THvLbKALnYHy8BGC1fvoqSW0lCh_Pt50AUlafDrXIZtMvnnc_PEHxMeb72hvEYhCycWhFNioi-kHZIXVMYOeRRf8QHyhxyIUzH7iCZuQz_eOloGKI2xRk3guUiCFhDodPI2CTns56xwX_4utQ=w2454-h218-no?authuser=0)


***Path: /src/app/_components/alert.component.ts***
The alert component passes alert messages to the template whenever a message is received from the alert service. It does this by subscribing to the alert services getMessage()  method which return an observable.
  ![enter image description here](https://lh3.googleusercontent.com/rrV52ZcSPMC1R0XkNwCiNCNERfzn40F6zuZjWwJyMKPh_Sjae_gQ7owa9LflIGWgChlHBOo-FubcSeA0lHYT1irVG5KXJyE86ZmHQD5M2CRuZPAGgcN4vP1pWKvwma1gI2fWvkNTh622d10KJKB98JlqC38U141Xy7xG0cNWvJ3IFZgE5R6Ahoq_VZDrpFQuo8kwZYm6zkC6tMfHgz5Uidqj6ZETYrPc6jXwnNwmTx_Xra-zg9r0i0WidxM0leBTrPjE0zTnTRXz6J11YeE2HFLaM0Mfji4VEjqg_IohK0-xrNnNc2MWD46wZKk86LM57fNwAhzJ_sNT_PEjCitfnHJFruA3OHgzydQdZM78B2K7XlNq_MLEVFMN5blzKIP90qWdnUlhwIIVAIS8HpiAN8Orpb6-w2pUgN7XF8K0qiih6YFiufeDNspupPZre854Ipv80_eDQo5AsXWTLLIq9ElqelX_AkKG41Mu7R24rosFYRWjSl9YUkHAoYqr0cRYDCpB0_5fipjo_6MJdRLJ2MIUKWrVk_Z75ovnMGGg9Tn94PnsckKSggWESoa5t4o-WOMFb32rmoXnRf0frcKDS_S_0T4-_FBe4eI-jEbSva3dfYLSllXUEJ9t8OGPvsgxb_HiKmhTIMeB6xBBhs5HYPV-wBPurxePyRnHs5pj4RrPCdw9XBE_6tmTv9C_6lHi24NOK1_Io_oHQsapDP211oMrIDgH3PsCISrWnJI56CMsdI3tzCcFlqE7cs3_Rw=w1214-h1142-no?authuser=0%22%29,%20url%28%22https://lh3.googleusercontent.com/rrV52ZcSPMC1R0XkNwCiNCNERfzn40F6zuZjWwJyMKPh_Sjae_gQ7owa9LflIGWgChlHBOo-FubcSeA0lHYT1irVG5KXJyE86ZmHQD5M2CRuZPAGgcN4vP1pWKvwma1gI2fWvkNTh622d10KJKB98JlqC38U141Xy7xG0cNWvJ3IFZgE5R6Ahoq_VZDrpFQuo8kwZYm6zkC6tMfHgz5Uidqj6ZETYrPc6jXwnNwmTx_Xra-zg9r0i0WidxM0leBTrPjE0zTnTRXz6J11YeE2HFLaM0Mfji4VEjqg_IohK0-xrNnNc2MWD46wZKk86LM57fNwAhzJ_sNT_PEjCitfnHJFruA3OHgzydQdZM78B2K7XlNq_MLEVFMN5blzKIP90qWdnUlhwIIVAIS8HpiAN8Orpb6-w2pUgN7XF8K0qiih6YFiufeDNspupPZre854Ipv80_eDQo5AsXWTLLIq9ElqelX_AkKG41Mu7R24rosFYRWjSl9YUkHAoYqr0cRYDCpB0_5fipjo_6MJdRLJ2MIUKWrVk_Z75ovnMGGg9Tn94PnsckKSggWESoa5t4o-WOMFb32rmoXnRf0frcKDS_S_0T4-_FBe4eI-jEbSva3dfYLSllXUEJ9t8OGPvsgxb_HiKmhTIMeB6xBBhs5HYPV-wBPurxePyRnHs5pj4RrPCdw9XBE_6tmTv9C_6lHi24NOK1_Io_oHQsapDP211oMrIDgH3PsCISrWnJI56CMsdI3tzCcFlqE7cs3_Rw=w327-h308-no?authuser=0)
    

***Path: /src/app/_service/alert.service.ts***
The alert service allows a show display results of success and  
waring. It can show allow designed page html (show on top and show on the bottom and left, right).
Function **getMessage()** method that return **Observable** should is used by the alert component to **Subscribe** pass notifications for whereever a message should be displaying.
![enter image description here](https://lh3.googleusercontent.com/ST9Of-Ux4xe7O2TnYLcdW04pQNTlWULNYXmGlOliO-q_MqcQybnDalApdkVIfA9CgOo5I9xLo_adyOFq9Wa4S9k50T0B1Muvy-EinkTy5icFHccjbo72fZCRObmVngaZPTIae487g0wAb758W6L52HTHx_g3RtIRZF-HVIEy0ga4OQ4CgdMaKj4VPJv-ac_A2yBuSv74VTOHbAyNYwt8oXVPhONyyGmDeLuy2v2N1Mto5627Hzt6NoUFBTuxitsNLocrv_17koY3nCIK7rc3IeUzEjDIXXfgtiAZtd73ujGSBV-OoFDNHwhuxaXKV8qCsl8enPTSAFUfKkWF2vLhq9bvlzj_nzW2K6mdVg15PdSFZhzCU00VoBXPg-fUrsS8DXlOhEQ4MYt9AKETIJGmzRZqZNPpfN1XNzpzMedgUsEaUZSjEagMbql682eCPfghAmIZrv3W0ntUqOXo_5uyuS3k50vKdNwFySeoFWODwNAs-dIkWmygZXEtBIIGEbZpras_-mPJYpR85yMNXdWivF9OkeKEAEttXCMAAMvxqRBDmOp8RKHlZAAFz361rt3Kjajl-hEfpYH1lixZcBcNPz1TMxs-uBNYUD3488n8_L-pXo8cBlwKfhm1Voufv19f1nNhCQDcuNgrhvqOQFmsUD8v2kLTmVudeShAU-GVQBEbUmea2Acujd3TSUWLeiFro2jhWOWSDxqKjXaFvXeL6O6qISN0EKY995ukSuBQnDIoSQZ-slQWJAZJR6rchg=w522-h300-no?authuser=0)
![enter image description here](https://lh3.googleusercontent.com/DghuP-N3FzYM9sa8bWp_aPZzwEiomkTIqqQJyd5P7y5ZNGdf81qGdF_J_fB-DPx8qTNbwCwo1lz0lJrAPASMp12DEWJoAUBg9l50prQMNi4ArLK5Mllo9dXFWkIqwDfde3JWPiYQHoibdfR8HOxUWKtYRbWY7z09synDtD_7J_wkTM9ocapig7YdNCdu3u2sDghaljQWohFq690uqmZ1IW8Iw43r-6B2fNgIQVowHiBY7sJ6ZSfQznZ6fwtzQLaoog3Kqy9GLAbBa5EB0E0q2YrepMF1drGu51mkFAYo39nXwScUy5wZAyHB009I5aGrF_9zZJe9oR1qJGLcq4d49JX6JRXgDO_oh7Q6PhzEtdzlXtNNxROV6tcfDv_ulbl5sAGrO49EHNogWrwnm1wsDZSOxCDnpMcj7qqm-5nMHXycpbEhCxev_kkHG2GoBUG1yJC7tx3ejqarfbZlxj2iPmehvaB_Z_Z7PgBiTTAqP62hBnIG8_NzByxvPS6f0SPrQG4_XWA_RZ8Es6cNlp2r0dWUAQljRcdVwFSb48OiUsvgujeMaFtbHE0JCvhGCDXl5lAcYvuJ6JySvtcgfOBSBlKLG4P2CHL24b9EtKEOTTh1ij6AxwpWBP9EIYWatBNbmouMMXggLlZMz2i4xicvyxv8juIyGk6Gp4JqdIzs1byBaAgKNnSHsUqtGfF7N7YhoK3kMuSkjymaqlgTF8XFCFeWnwXlCxWvffKmD3tMH44EXahUCHY1aZqbDvebLw=w640-h300-no?authuser=0)
![enter image description here](https://lh3.googleusercontent.com/G143LAQPk1QtOuDH_wJ_SsFkt3pSs-Wmwn3ym1gmx4KUbGjnU2REek26X8GjBzFYHJ0tGCFZwekhytjgCdS2Y93mySUTg2ldtG2u5cvQQ7yZI_NzOTSJQjTf7O2dkcZXB7N9TZjEHMBKe-IBcO0GpISyDHll0rwG1WvOsAFYfmI3rf-qntz-SnfxWcvTsjOyy8Sm704333daz0DTQagFJjvFKm6N1NB70hRx5NJ5urqCAXEbZ_aN1ameYbkn8WspH7V3OHagQFfcR_gnhWHGN6RW7gpFIPVh-xuR0qhrbXeAsneFfOcqleUYvqtZ9FzJ6OIxsF7s0YBBhgQ_5Kgk5ufpQofxpkKLQbWV5dD07sI2EGSUWEv0ncwD_PY95gOVZ3263XaqG68WBoh6OBoxtq8U7KUBUXXR7Bor6xAqANLQcc62EfakY1_VTq7LYWVN-DXxRHt0Y7_uGRGm_ZX2rlvaD1pSXD-HfU6UZyrTHgGY34XimhmGO6kGHdMsaps-vA3Z-rZEPVpEZpc1GFC44PKYfo-tD9RniqdXg9SZmSdMEsfk4--Xx-FDe0glNdMuN-QUtgWQpq5UnRn2-DeXgKoIw3_qbIfPpsgGzAY_mY9uX8Nj0XfBUEkGgVDdIM-2CwBNPxSMLbYvA6cGjwQc06R1Y9-7KmvZ4M6MpHDC2DrbQGBhW7dEz2tOHrwT2lSYgsX91D7xyL9YV-6hKCsN2l-5NuHBQB9MTXaVE85SwcEyIm1fE_BD0IPusZvtxw=w654-h300-no?authuser=0)

![enter image description here](https://lh3.googleusercontent.com/Hka_vxySq7fnEbKAwxtKSfe8CoYCCnI1m6yU0XuXI5lUKd0Csr4P1h6xBoVtjy4PCt53B3GEIZSl85IoANfSiPWnWhAHomDiMD31GhPg6Gh2aIk_NSy1BtPEw6A4Ug8LAlp-psH3Z2l5nj0QLXSJO8WH0D7oGYE84oEkNoKlFAapYXvnMF1-W5Ym0JODkphywHpq2w4sCuMqYVUmrm246qKQ52jDzwDgbFUxw5tzMTFRW5Ospfd-LowE0wIJkNu8zDAlw5g7pE1K0aFYhdc2D-yEihmjel-ThMpJSfSKz93cjGyEPRcWLCemG8OyF1wI0FziS-xKYUT28bcqI7sY0sDigmIxvdgSJHbN8xA8pnxzERRRaMTfMLoHN_r-oorIjnil56e7XuCfN2RVAvwFLOel7kqLSUAjkmPe4Vq2BYet3jcdd4xrh1T1cJk9CH9bttNWYWVbEjtt9Ixv5ac8q_5hOCQC65nk8tmc8sNRwQoxZVy6Z7Gn0TZvo4d7ZxvM5SknpPtRpZ5vkp3IlkVC1qoAEvXpMs1Pzlniiu5jYKgHZQgjP8SlrRKKNM02MUZf6muB5hisoaYmQ5Zq75Ju0PFQUq80uHAjsJOrkyAeBBOeJoOBHt6VT9PArkUlaI26A9I7ZHwsgUe3EximxpFj1fDYBnMaXxX_4bMQ3SWF_7hlMlRYjnzXI5cME4KnUlj7QU7u1le382fqn2iM9XTR_6coFlyetzFSNwr4bacJ2vb7wz6T8FVuaVT7LM75Sw=w818-h300-no?authuser=0)

## Download Service

***Path: /src/app/_service/download.service.ts***
The download service contains  **Get all data file and Download file methods** for managing, It acts as the interface between the Angular application and the backend API.
