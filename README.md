This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more (56) external
libraries included.

Static <b>ffmpeg v4.3.1</b> build from this repository currently compiles on:
<table>
<!-- tr><td><b>CentOS 7.5-1804</b>   </td><td>x86_64</td -->
<tr><td><b>Ubuntu 18.04.1 LTS</b></td><td>amd64</td>
<td rowspan="3">
<img src="http://www.movieconverter-studio.com/_PUBLIC/ffmpeg/logo-new/ffmpeg-logo-src/ffmpeg-logo.png" height="90">
</td></tr>
<!-- tr><td><b>Debian 9.5</b>        </td><td>amd64</td></tr -->
</table>

For build see [BUILD.md].

Included features in this build of ffmpeg are:
<pre>
ffmpeg version            4.3.1
C compiler                gcc
C library                 glibc
big-endian                no
runtime cpu detection     yes
standalone assembly       yes
x86 assembler             nasm
MMX enabled               yes
MMXEXT enabled            yes
3DNow! enabled            yes
3DNow! extended enabled   yes
SSE enabled               yes
SSSE3 enabled             yes
AESNI enabled             yes
AVX enabled               yes
AVX2 enabled              yes
AVX-512 enabled           yes
XOP enabled               yes
FMA3 enabled              yes
FMA4 enabled              yes
i686 features enabled     yes
CMOV is fast              yes
EBX available             yes
EBP available             yes
debug symbols             no
strip symbols             yes
optimize for size         no
optimizations             yes
static                    yes
shared                    no
postprocessing support    yes
network support           yes
threading support         pthreads
safe bitstream reader     yes
texi2html enabled         no
perl enabled              yes
pod2man enabled           yes
makeinfo enabled          no
makeinfo supports HTML    no

External libraries:
bzlib                   libmodplug              libvpx
frei0r                  libmp3lame              libwavpack
iconv                   libopencore_amrnb       libwebp
libass                  libopencore_amrwb       libx264
libbluray               libopenjpeg             libx265
libbs2b                 libopus                 libxavs
libcaca                 librtmp                 libxcb
libcdio                 libshine                libxcb_shape
libdc1394               libsoxr                 libxcb_shm
libfdk_aac              libspeex                libxcb_xfixes
libflite                libtheora               libxvid
libfontconfig           libtwolame              libzmq
libfreetype             libv4l2                 libzvbi
libgsm                  libvidstab              lzma
libiec61883             libvo_amrwbenc          xlib
libilbc                 libvorbis               zlib

External libraries providing hardware acceleration:
v4l2_m2m

Libraries:
avcodec                 avformat                swresample
avdevice                avutil                  swscale
avfilter                postproc

Programs:
ffmpeg                  ffprobe

Enabled decoders:
aac                     flv                     pcm_u32le
aac_fixed               fmvc                    pcm_u8
aac_latm                fourxm                  pcm_vidc
aasc                    fraps                   pcx
ac3                     frwu                    pfm
ac3_fixed               g2m                     pgm
acelp_kelvin            g723_1                  pgmyuv
adpcm_4xm               g729                    pgssub
adpcm_adx               gdv                     pictor
adpcm_afc               gif                     pixlet
adpcm_agm               gremlin_dpcm            pjs
adpcm_aica              gsm                     png
adpcm_argo              gsm_ms                  ppm
adpcm_ct                h261                    prores
adpcm_dtk               h263                    prosumer
adpcm_ea                h263_v4l2m2m            psd
adpcm_ea_maxis_xa       h263i                   ptx
adpcm_ea_r1             h263p                   qcelp
adpcm_ea_r2             h264                    qdm2
adpcm_ea_r3             h264_v4l2m2m            qdmc
adpcm_ea_xas            hap                     qdraw
adpcm_g722              hca                     qpeg
adpcm_g726              hcom                    qtrle
adpcm_g726le            hevc                    r10k
adpcm_ima_alp           hevc_v4l2m2m            r210
adpcm_ima_amv           hnm4_video              ra_144
adpcm_ima_apc           hq_hqa                  ra_288
adpcm_ima_apm           hqx                     ralf
adpcm_ima_cunning       huffyuv                 rasc
adpcm_ima_dat4          hymt                    rawvideo
adpcm_ima_dk3           iac                     realtext
adpcm_ima_dk4           idcin                   rl2
adpcm_ima_ea_eacs       idf                     roq
adpcm_ima_ea_sead       iff_ilbm                roq_dpcm
adpcm_ima_iss           ilbc                    rpza
adpcm_ima_mtf           imc                     rscc
adpcm_ima_oki           imm4                    rv10
adpcm_ima_qt            imm5                    rv20
adpcm_ima_rad           indeo2                  rv30
adpcm_ima_smjpeg        indeo3                  rv40
adpcm_ima_ssi           indeo4                  s302m
adpcm_ima_wav           indeo5                  sami
adpcm_ima_ws            interplay_acm           sanm
adpcm_ms                interplay_dpcm          sbc
adpcm_mtaf              interplay_video         scpr
adpcm_psx               jacosub                 screenpresso
adpcm_sbpro_2           jpeg2000                sdx2_dpcm
adpcm_sbpro_3           jpegls                  sgi
adpcm_sbpro_4           jv                      sgirle
adpcm_swf               kgv1                    sheervideo
adpcm_thp               kmvc                    shorten
adpcm_thp_le            lagarith                sipr
adpcm_vima              libfdk_aac              siren
adpcm_xa                libgsm                  smackaud
adpcm_yamaha            libgsm_ms               smacker
adpcm_zork              libilbc                 smc
agm                     libopencore_amrnb       smvjpeg
aic                     libopencore_amrwb       snow
alac                    libopenjpeg             sol_dpcm
alias_pix               libopus                 sonic
als                     libspeex                sp5x
amrnb                   libvorbis               speedhq
amrwb                   libvpx_vp8              srgc
amv                     libvpx_vp9              srt
anm                     libzvbi_teletext        ssa
ansi                    loco                    stl
ape                     lscr                    subrip
apng                    m101                    subviewer
aptx                    mace3                   subviewer1
aptx_hd                 mace6                   sunrast
arbc                    magicyuv                svq1
ass                     mdec                    svq3
asv1                    metasound               tak
asv2                    microdvd                targa
atrac1                  mimic                   targa_y216
atrac3                  mjpeg                   tdsc
atrac3al                mjpegb                  text
atrac3p                 mlp                     theora
atrac3pal               mmvideo                 thp
atrac9                  motionpixels            tiertexseqvideo
aura                    movtext                 tiff
aura2                   mp1                     tmv
avrn                    mp1float                truehd
avrp                    mp2                     truemotion1
avs                     mp2float                truemotion2
avui                    mp3                     truemotion2rt
ayuv                    mp3adu                  truespeech
bethsoftvid             mp3adufloat             tscc
bfi                     mp3float                tscc2
bink                    mp3on4                  tta
binkaudio_dct           mp3on4float             twinvq
binkaudio_rdft          mpc7                    txd
bintext                 mpc8                    ulti
bitpacked               mpeg1_v4l2m2m           utvideo
bmp                     mpeg1video              v210
bmv_audio               mpeg2_v4l2m2m           v210x
bmv_video               mpeg2video              v308
brender_pix             mpeg4                   v408
c93                     mpeg4_v4l2m2m           v410
cavs                    mpegvideo               vb
ccaption                mpl2                    vble
cdgraphics              msa1                    vc1
cdtoons                 mscc                    vc1_v4l2m2m
cdxl                    msmpeg4v1               vc1image
cfhd                    msmpeg4v2               vcr1
cinepak                 msmpeg4v3               vmdaudio
clearvideo              msrle                   vmdvideo
cljr                    mss1                    vmnc
cllc                    mss2                    vorbis
comfortnoise            msvideo1                vp3
cook                    mszh                    vp4
cpia                    mts2                    vp5
cscd                    mv30                    vp6
cyuv                    mvc1                    vp6a
dca                     mvc2                    vp6f
dds                     mvdv                    vp7
derf_dpcm               mvha                    vp8
dfa                     mwsc                    vp8_v4l2m2m
dirac                   mxpeg                   vp9
dnxhd                   nellymoser              vp9_v4l2m2m
dolby_e                 notchlc                 vplayer
dpx                     nuv                     vqa
dsd_lsbf                on2avc                  wavpack
dsd_lsbf_planar         opus                    wcmv
dsd_msbf                paf_audio               webp
dsd_msbf_planar         paf_video               webvtt
dsicinaudio             pam                     wmalossless
dsicinvideo             pbm                     wmapro
dss_sp                  pcm_alaw                wmav1
dst                     pcm_bluray              wmav2
dvaudio                 pcm_dvd                 wmavoice
dvbsub                  pcm_f16le               wmv1
dvdsub                  pcm_f24le               wmv2
dvvideo                 pcm_f32be               wmv3
dxa                     pcm_f32le               wmv3image
dxtory                  pcm_f64be               wnv1
dxv                     pcm_f64le               wrapped_avframe
eac3                    pcm_lxf                 ws_snd1
eacmv                   pcm_mulaw               xan_dpcm
eamad                   pcm_s16be               xan_wc3
eatgq                   pcm_s16be_planar        xan_wc4
eatgv                   pcm_s16le               xbin
eatqi                   pcm_s16le_planar        xbm
eightbps                pcm_s24be               xface
eightsvx_exp            pcm_s24daud             xl
eightsvx_fib            pcm_s24le               xma1
escape124               pcm_s24le_planar        xma2
escape130               pcm_s32be               xpm
evrc                    pcm_s32le               xsub
exr                     pcm_s32le_planar        xwd
ffv1                    pcm_s64be               y41p
ffvhuff                 pcm_s64le               ylc
ffwavesynth             pcm_s8                  yop
fic                     pcm_s8_planar           yuv4
fits                    pcm_u16be               zero12v
flac                    pcm_u16le               zerocodec
flashsv                 pcm_u24be               zlib
flashsv2                pcm_u24le               zmbv
flic                    pcm_u32be

Enabled encoders:
a64multi                libopenjpeg             pcm_u32be
a64multi5               libopus                 pcm_u32le
aac                     libshine                pcm_u8
ac3                     libspeex                pcm_vidc
ac3_fixed               libtheora               pcx
adpcm_adx               libtwolame              pgm
adpcm_g722              libvo_amrwbenc          pgmyuv
adpcm_g726              libvorbis               png
adpcm_g726le            libvpx_vp8              ppm
adpcm_ima_qt            libvpx_vp9              prores
adpcm_ima_ssi           libwavpack              prores_aw
adpcm_ima_wav           libwebp                 prores_ks
adpcm_ms                libwebp_anim            qtrle
adpcm_swf               libx264                 r10k
adpcm_yamaha            libx264rgb              r210
alac                    libx265                 ra_144
alias_pix               libxavs                 rawvideo
amv                     libxvid                 roq
apng                    ljpeg                   roq_dpcm
aptx                    magicyuv                rv10
aptx_hd                 mjpeg                   rv20
ass                     mlp                     s302m
asv1                    movtext                 sbc
asv2                    mp2                     sgi
avrp                    mp2fixed                snow
avui                    mpeg1video              sonic
ayuv                    mpeg2video              sonic_ls
bmp                     mpeg4                   srt
cinepak                 mpeg4_v4l2m2m           ssa
cljr                    msmpeg4v2               subrip
comfortnoise            msmpeg4v3               sunrast
dca                     msvideo1                svq1
dnxhd                   nellymoser              targa
dpx                     opus                    text
dvbsub                  pam                     tiff
dvdsub                  pbm                     truehd
dvvideo                 pcm_alaw                tta
eac3                    pcm_dvd                 utvideo
ffv1                    pcm_f32be               v210
ffvhuff                 pcm_f32le               v308
fits                    pcm_f64be               v408
flac                    pcm_f64le               v410
flashsv                 pcm_mulaw               vc2
flashsv2                pcm_s16be               vorbis
flv                     pcm_s16be_planar        vp8_v4l2m2m
g723_1                  pcm_s16le               wavpack
gif                     pcm_s16le_planar        webvtt
h261                    pcm_s24be               wmav1
h263                    pcm_s24daud             wmav2
h263_v4l2m2m            pcm_s24le               wmv1
h263p                   pcm_s24le_planar        wmv2
h264_v4l2m2m            pcm_s32be               wrapped_avframe
hevc_v4l2m2m            pcm_s32le               xbm
huffyuv                 pcm_s32le_planar        xface
jpeg2000                pcm_s64be               xsub
jpegls                  pcm_s64le               xwd
libfdk_aac              pcm_s8                  y41p
libgsm                  pcm_s8_planar           yuv4
libgsm_ms               pcm_u16be               zlib
libilbc                 pcm_u16le               zmbv
libmp3lame              pcm_u24be
libopencore_amrnb       pcm_u24le

Enabled hwaccels:

Enabled parsers:
aac                     dvdsub                  opus
aac_latm                flac                    png
ac3                     g723_1                  pnm
adx                     g729                    rv30
av1                     gif                     rv40
avs2                    gsm                     sbc
bmp                     h261                    sipr
cavsvideo               h263                    tak
cook                    h264                    vc1
dca                     hevc                    vorbis
dirac                   jpeg2000                vp3
dnxhd                   mjpeg                   vp8
dpx                     mlp                     vp9
dvaudio                 mpeg4video              webp
dvbsub                  mpegaudio               xma
dvd_nav                 mpegvideo

Enabled demuxers:
aa                      hnm                     pcm_s24le
aac                     ico                     pcm_s32be
ac3                     idcin                   pcm_s32le
acm                     idf                     pcm_s8
act                     iff                     pcm_u16be
adf                     ifv                     pcm_u16le
adp                     ilbc                    pcm_u24be
ads                     image2                  pcm_u24le
adx                     image2_alias_pix        pcm_u32be
aea                     image2_brender_pix      pcm_u32le
afc                     image2pipe              pcm_u8
aiff                    image_bmp_pipe          pcm_vidc
aix                     image_dds_pipe          pjs
alp                     image_dpx_pipe          pmp
amr                     image_exr_pipe          pp_bnk
amrnb                   image_gif_pipe          pva
amrwb                   image_j2k_pipe          pvf
anm                     image_jpeg_pipe         qcp
apc                     image_jpegls_pipe       r3d
ape                     image_pam_pipe          rawvideo
apm                     image_pbm_pipe          realtext
apng                    image_pcx_pipe          redspark
aptx                    image_pgm_pipe          rl2
aptx_hd                 image_pgmyuv_pipe       rm
aqtitle                 image_pictor_pipe       roq
argo_asf                image_png_pipe          rpl
asf                     image_ppm_pipe          rsd
asf_o                   image_psd_pipe          rso
ass                     image_qdraw_pipe        rtp
ast                     image_sgi_pipe          rtsp
au                      image_sunrast_pipe      s337m
av1                     image_svg_pipe          sami
avi                     image_tiff_pipe         sap
avr                     image_webp_pipe         sbc
avs                     image_xpm_pipe          sbg
avs2                    image_xwd_pipe          scc
bethsoftvid             ingenient               sdp
bfi                     ipmovie                 sdr2
bfstm                   ircam                   sds
bink                    iss                     sdx
bintext                 iv8                     segafilm
bit                     ivf                     ser
bmv                     ivr                     shorten
boa                     jacosub                 siff
brstm                   jv                      sln
c93                     kux                     smacker
caf                     kvag                    smjpeg
cavsvideo               libmodplug              smush
cdg                     live_flv                sol
cdxl                    lmlm4                   sox
cine                    loas                    spdif
codec2                  lrc                     srt
codec2raw               lvf                     stl
concat                  lxf                     str
data                    m4v                     subviewer
daud                    matroska                subviewer1
dcstr                   mgsts                   sup
derf                    microdvd                svag
dfa                     mjpeg                   swf
dhav                    mjpeg_2000              tak
dirac                   mlp                     tedcaptions
dnxhd                   mlv                     thp
dsf                     mm                      threedostr
dsicin                  mmf                     tiertexseq
dss                     mov                     tmv
dts                     mp3                     truehd
dtshd                   mpc                     tta
dv                      mpc8                    tty
dvbsub                  mpegps                  txd
dvbtxt                  mpegts                  ty
dxa                     mpegtsraw               v210
ea                      mpegvideo               v210x
ea_cdata                mpjpeg                  vag
eac3                    mpl2                    vc1
epaf                    mpsub                   vc1t
ffmetadata              msf                     vividas
filmstrip               msnwc_tcp               vivo
fits                    mtaf                    vmd
flac                    mtv                     vobsub
flic                    musx                    voc
flv                     mv                      vpk
fourxm                  mvi                     vplayer
frm                     mxf                     vqf
fsb                     mxg                     w64
fwse                    nc                      wav
g722                    nistsphere              wc3
g723_1                  nsp                     webm_dash_manifest
g726                    nsv                     webvtt
g726le                  nut                     wsaud
g729                    nuv                     wsd
gdv                     ogg                     wsvqa
genh                    oma                     wtv
gif                     paf                     wv
gsm                     pcm_alaw                wve
gxf                     pcm_f32be               xa
h261                    pcm_f32le               xbin
h263                    pcm_f64be               xmv
h264                    pcm_f64le               xvag
hca                     pcm_mulaw               xwma
hcom                    pcm_s16be               yop
hevc                    pcm_s16le               yuv4mpegpipe
hls                     pcm_s24be

Enabled muxers:
a64                     hls                     pcm_s32be
ac3                     ico                     pcm_s32le
adts                    ilbc                    pcm_s8
adx                     image2                  pcm_u16be
aiff                    image2pipe              pcm_u16le
amr                     ipod                    pcm_u24be
apng                    ircam                   pcm_u24le
aptx                    ismv                    pcm_u32be
aptx_hd                 ivf                     pcm_u32le
asf                     jacosub                 pcm_u8
asf_stream              kvag                    pcm_vidc
ass                     latm                    psp
ast                     lrc                     rawvideo
au                      m4v                     rm
avi                     matroska                roq
avm2                    matroska_audio          rso
avs2                    md5                     rtp
bit                     microdvd                rtp_mpegts
caf                     mjpeg                   rtsp
cavsvideo               mkvtimestamp_v2         sap
codec2                  mlp                     sbc
codec2raw               mmf                     scc
crc                     mov                     segafilm
dash                    mp2                     segment
data                    mp3                     singlejpeg
daud                    mp4                     smjpeg
dirac                   mpeg1system             smoothstreaming
dnxhd                   mpeg1vcd                sox
dts                     mpeg1video              spdif
dv                      mpeg2dvd                spx
eac3                    mpeg2svcd               srt
f4v                     mpeg2video              stream_segment
ffmetadata              mpeg2vob                streamhash
fifo                    mpegts                  sup
fifo_test               mpjpeg                  swf
filmstrip               mxf                     tee
fits                    mxf_d10                 tg2
flac                    mxf_opatom              tgp
flv                     null                    truehd
framecrc                nut                     tta
framehash               oga                     uncodedframecrc
framemd5                ogg                     vc1
g722                    ogv                     vc1t
g723_1                  oma                     voc
g726                    opus                    w64
g726le                  pcm_alaw                wav
gif                     pcm_f32be               webm
gsm                     pcm_f32le               webm_chunk
gxf                     pcm_f64be               webm_dash_manifest
h261                    pcm_f64le               webp
h263                    pcm_mulaw               webvtt
h264                    pcm_s16be               wtv
hash                    pcm_s16le               wv
hds                     pcm_s24be               yuv4mpegpipe
hevc                    pcm_s24le

Enabled protocols:
async                   httpproxy               pipe
bluray                  icecast                 prompeg
cache                   librtmp                 rtp
concat                  librtmpe                srtp
crypto                  librtmps                subfile
data                    librtmpt                tcp
file                    librtmpte               tee
ftp                     libzmq                  udp
gopher                  md5                     udplite
hls                     mmsh                    unix
http                    mmst

Enabled filters:
abench                  dedot                   paletteuse
abitscope               deesser                 pan
acompressor             deflate                 perms
acontrast               deflicker               perspective
acopy                   dejudder                phase
acrossfade              delogo                  photosensitivity
acrossover              derain                  pixdesctest
acrusher                deshake                 pixscope
acue                    despill                 pp
addroi                  detelecine              pp7
adeclick                dilation                premultiply
adeclip                 displace                prewitt
adelay                  dnn_processing          pseudocolor
aderivative             doubleweave             psnr
adrawgraph              drawbox                 pullup
aecho                   drawgraph               qp
aemphasis               drawgrid                random
aeval                   drawtext                readeia608
aevalsrc                drmeter                 readvitc
afade                   dynaudnorm              realtime
afftdn                  earwax                  remap
afftfilt                ebur128                 removegrain
afifo                   edgedetect              removelogo
afir                    elbg                    repeatfields
afirsrc                 entropy                 replaygain
aformat                 eq                      reverse
agate                   equalizer               rgbashift
agraphmonitor           erosion                 rgbtestsrc
ahistogram              extractplanes           roberts
aiir                    extrastereo             rotate
aintegral               fade                    sab
ainterleave             fftdnoiz                scale
alimiter                fftfilt                 scale2ref
allpass                 field                   scdet
allrgb                  fieldhint               scroll
allyuv                  fieldmatch              select
aloop                   fieldorder              selectivecolor
alphaextract            fifo                    sendcmd
alphamerge              fillborders             separatefields
amerge                  find_rect               setdar
ametadata               firequalizer            setfield
amix                    flanger                 setparams
amovie                  flite                   setpts
amplify                 floodfill               setrange
amultiply               format                  setsar
anequalizer             fps                     settb
anlmdn                  framepack               showcqt
anlms                   framerate               showfreqs
anoisesrc               framestep               showinfo
anull                   freezedetect            showpalette
anullsink               freezeframes            showspatial
anullsrc                frei0r                  showspectrum
apad                    frei0r_src              showspectrumpic
aperms                  fspp                    showvolume
aphasemeter             gblur                   showwaves
aphaser                 geq                     showwavespic
apulsator               gradfun                 shuffleframes
arealtime               gradients               shuffleplanes
aresample               graphmonitor            sidechaincompress
areverse                greyedge                sidechaingate
arnndn                  haas                    sidedata
aselect                 haldclut                sierpinski
asendcmd                haldclutsrc             signalstats
asetnsamples            hdcd                    signature
asetpts                 headphone               silencedetect
asetrate                hflip                   silenceremove
asettb                  highpass                sinc
ashowinfo               highshelf               sine
asidedata               hilbert                 smartblur
asoftclip               histeq                  smptebars
asplit                  histogram               smptehdbars
ass                     hqdn3d                  sobel
astats                  hqx                     spectrumsynth
astreamselect           hstack                  split
asubboost               hue                     spp
atadenoise              hwdownload              sr
atempo                  hwmap                   ssim
atrim                   hwupload                stereo3d
avectorscope            hysteresis              stereotools
avgblur                 idet                    stereowiden
axcorrelate             il                      streamselect
azmq                    inflate                 subtitles
bandpass                interlace               super2xsai
bandreject              interleave              superequalizer
bass                    join                    surround
bbox                    kerndeint               swaprect
bench                   lagfun                  swapuv
bilateral               lenscorrection          tblend
biquad                  life                    telecine
bitplanenoise           limiter                 testsrc
blackdetect             loop                    testsrc2
blackframe              loudnorm                thistogram
blend                   lowpass                 threshold
bm3d                    lowshelf                thumbnail
boxblur                 lumakey                 tile
bs2b                    lut                     tinterlace
bwdif                   lut1d                   tlut2
cas                     lut2                    tmedian
cellauto                lut3d                   tmix
channelmap              lutrgb                  tonemap
channelsplit            lutyuv                  tpad
chorus                  mandelbrot              transpose
chromahold              maskedclamp             treble
chromakey               maskedmax               tremolo
chromashift             maskedmerge             trim
ciescope                maskedmin               unpremultiply
codecview               maskedthreshold         unsharp
color                   maskfun                 untile
colorbalance            mcdeint                 uspp
colorchannelmixer       mcompand                v360
colorhold               median                  vaguedenoiser
colorkey                mergeplanes             vectorscope
colorlevels             mestimate               vflip
colormatrix             metadata                vfrdet
colorspace              midequalizer            vibrance
compand                 minterpolate            vibrato
compensationdelay       mix                     vidstabdetect
concat                  movie                   vidstabtransform
convolution             mpdecimate              vignette
convolve                mptestsrc               vmafmotion
copy                    negate                  volume
cover_rect              nlmeans                 volumedetect
crop                    nnedi                   vstack
cropdetect              noformat                w3fdif
crossfeed               noise                   waveform
crystalizer             normalize               weave
cue                     null                    xbr
curves                  nullsink                xfade
datascope               nullsrc                 xmedian
dblur                   oscilloscope            xstack
dcshift                 overlay                 yadif
dctdnoiz                owdenoise               yaepblur
deband                  pad                     yuvtestsrc
deblock                 pal100bars              zmq
decimate                pal75bars               zoompan
deconvolve              palettegen

Enabled bsfs:
aac_adtstoasc           h264_redundant_pps      null
av1_frame_merge         hapqa_extract           opus_metadata
av1_frame_split         hevc_metadata           pcm_rechunk
av1_metadata            hevc_mp4toannexb        prores_metadata
chomp                   imx_dump_header         remove_extradata
dca_core                mjpeg2jpeg              text2movsub
dump_extradata          mjpega_dump_header      trace_headers
eac3_core               mov2textsub             truehd_core
extract_extradata       mp3_header_decompress   vp9_metadata
filter_units            mpeg2_metadata          vp9_raw_reorder
h264_metadata           mpeg4_unpack_bframes    vp9_superframe
h264_mp4toannexb        noise                   vp9_superframe_split

Enabled indevs:
fbdev                   libcdio                 v4l2
iec61883                libdc1394               xcbgrab
lavfi                   oss

Enabled outdevs:
caca                    oss                     xv
fbdev                   v4l2
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
