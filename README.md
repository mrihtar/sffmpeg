This repository is an extended clone of https://github.com/pyke369/sffmpeg  
It builds a static version of ffmpeg executable with a lot more (56) external
libraries included.

Static <b>ffmpeg v4.1</b> build from this repository currently compiles on:
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
ffmpeg version            4.1
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
bzlib			libmodplug		libvpx
frei0r			libmp3lame		libwavpack
iconv			libopencore_amrnb	libwebp
libass			libopencore_amrwb	libx264
libbluray		libopenjpeg		libx265
libbs2b			libopus			libxavs
libcaca			librtmp			libxcb
libcdio			libshine		libxcb_shape
libdc1394		libsoxr			libxcb_shm
libfdk_aac		libspeex		libxcb_xfixes
libflite		libtheora		libxvid
libfontconfig		libtwolame		libzmq
libfreetype		libv4l2			libzvbi
libgsm			libvidstab		lzma
libiec61883		libvo_amrwbenc		xlib
libilbc			libvorbis		zlib

External libraries providing hardware acceleration:
v4l2_m2m

Libraries:
avcodec			avformat		swresample
avdevice		avutil			swscale
avfilter		postproc

Programs:
ffmpeg			ffprobe

Enabled decoders:
aac			atrac3p			eightsvx_fib
aac_fixed		atrac3pal		escape124
aac_latm		atrac9			escape130
aasc			aura			evrc
ac3			aura2			exr
ac3_fixed		avrn			ffv1
adpcm_4xm		avrp			ffvhuff
adpcm_adx		avs			ffwavesynth
adpcm_afc		avui			fic
adpcm_aica		ayuv			fits
adpcm_ct		bethsoftvid		flac
adpcm_dtk		bfi			flashsv
adpcm_ea		bink			flashsv2
adpcm_ea_maxis_xa	binkaudio_dct		flic
adpcm_ea_r1		binkaudio_rdft		flv
adpcm_ea_r2		bintext			fmvc
adpcm_ea_r3		bitpacked		fourxm
adpcm_ea_xas		bmp			fraps
adpcm_g722		bmv_audio		frwu
adpcm_g726		bmv_video		g2m
adpcm_g726le		brender_pix		g723_1
adpcm_ima_amv		c93			g729
adpcm_ima_apc		cavs			gdv
adpcm_ima_dat4		ccaption		gif
adpcm_ima_dk3		cdgraphics		gremlin_dpcm
adpcm_ima_dk4		cdxl			gsm
adpcm_ima_ea_eacs	cfhd			gsm_ms
adpcm_ima_ea_sead	cinepak			h261
adpcm_ima_iss		clearvideo		h263
adpcm_ima_oki		cljr			h263_v4l2m2m
adpcm_ima_qt		cllc			h263i
adpcm_ima_rad		comfortnoise		h263p
adpcm_ima_smjpeg	cook			h264
adpcm_ima_wav		cpia			h264_v4l2m2m
adpcm_ima_ws		cscd			hap
adpcm_ms		cyuv			hevc
adpcm_mtaf		dca			hnm4_video
adpcm_psx		dds			hq_hqa
adpcm_sbpro_2		dfa			hqx
adpcm_sbpro_3		dirac			huffyuv
adpcm_sbpro_4		dnxhd			iac
adpcm_swf		dolby_e			idcin
adpcm_thp		dpx			idf
adpcm_thp_le		dsd_lsbf		iff_ilbm
adpcm_vima		dsd_lsbf_planar		ilbc
adpcm_xa		dsd_msbf		imc
adpcm_yamaha		dsd_msbf_planar		imm4
aic			dsicinaudio		indeo2
alac			dsicinvideo		indeo3
alias_pix		dss_sp			indeo4
als			dst			indeo5
amrnb			dvaudio			interplay_acm
amrwb			dvbsub			interplay_dpcm
amv			dvdsub			interplay_video
anm			dvvideo			jacosub
ansi			dxa			jpeg2000
ape			dxtory			jpegls
apng			dxv			jv
aptx			eac3			kgv1
aptx_hd			eacmv			kmvc
ass			eamad			lagarith
asv1			eatgq			libfdk_aac
asv2			eatgv			libgsm
atrac1			eatqi			libgsm_ms
atrac3			eightbps		libilbc
atrac3al		eightsvx_exp		libopencore_amrnb
libopencore_amrwb	pcm_alaw		rscc
libopenjpeg		pcm_bluray		rv10
libopus			pcm_dvd			rv20
libspeex		pcm_f16le		rv30
libvorbis		pcm_f24le		rv40
libvpx_vp8		pcm_f32be		s302m
libvpx_vp9		pcm_f32le		sami
libzvbi_teletext	pcm_f64be		sanm
loco			pcm_f64le		sbc
m101			pcm_lxf			scpr
mace3			pcm_mulaw		screenpresso
mace6			pcm_s16be		sdx2_dpcm
magicyuv		pcm_s16be_planar	sgi
mdec			pcm_s16le		sgirle
metasound		pcm_s16le_planar	sheervideo
microdvd		pcm_s24be		shorten
mimic			pcm_s24daud		sipr
mjpeg			pcm_s24le		smackaud
mjpegb			pcm_s24le_planar	smacker
mlp			pcm_s32be		smc
mmvideo			pcm_s32le		smvjpeg
motionpixels		pcm_s32le_planar	snow
movtext			pcm_s64be		sol_dpcm
mp1			pcm_s64le		sonic
mp1float		pcm_s8			sp5x
mp2			pcm_s8_planar		speedhq
mp2float		pcm_u16be		srgc
mp3			pcm_u16le		srt
mp3adu			pcm_u24be		ssa
mp3adufloat		pcm_u24le		stl
mp3float		pcm_u32be		subrip
mp3on4			pcm_u32le		subviewer
mp3on4float		pcm_u8			subviewer1
mpc7			pcm_vidc		sunrast
mpc8			pcm_zork		svq1
mpeg1_v4l2m2m		pcx			svq3
mpeg1video		pgm			tak
mpeg2_v4l2m2m		pgmyuv			targa
mpeg2video		pgssub			targa_y216
mpeg4			pictor			tdsc
mpeg4_v4l2m2m		pixlet			text
mpegvideo		pjs			theora
mpl2			png			thp
msa1			ppm			tiertexseqvideo
mscc			prores			tiff
msmpeg4v1		prosumer		tmv
msmpeg4v2		psd			truehd
msmpeg4v3		ptx			truemotion1
msrle			qcelp			truemotion2
mss1			qdm2			truemotion2rt
mss2			qdmc			truespeech
msvideo1		qdraw			tscc
mszh			qpeg			tscc2
mts2			qtrle			tta
mvc1			r10k			twinvq
mvc2			r210			txd
mwsc			ra_144			ulti
mxpeg			ra_288			utvideo
nellymoser		ralf			v210
nuv			rasc			v210x
on2avc			rawvideo		v308
opus			realtext		v408
paf_audio		rl2			v410
paf_video		roq			vb
pam			roq_dpcm		vble
pbm			rpza			vc1
vc1_v4l2m2m		wavpack			xan_wc4
vc1image		wcmv			xbin
vcr1			webp			xbm
vmdaudio		webvtt			xface
vmdvideo		wmalossless		xl
vmnc			wmapro			xma1
vorbis			wmav1			xma2
vp3			wmav2			xpm
vp5			wmavoice		xsub
vp6			wmv1			xwd
vp6a			wmv2			y41p
vp6f			wmv3			ylc
vp7			wmv3image		yop
vp8			wnv1			yuv4
vp8_v4l2m2m		wrapped_avframe		zero12v
vp9			ws_snd1			zerocodec
vp9_v4l2m2m		xan_dpcm		zlib
vplayer			xan_wc3			zmbv
vqa

Enabled encoders:
a64multi		libopus			pcm_u32be
a64multi5		libshine		pcm_u32le
aac			libspeex		pcm_u8
ac3			libtheora		pcm_vidc
ac3_fixed		libtwolame		pcx
adpcm_adx		libvo_amrwbenc		pgm
adpcm_g722		libvorbis		pgmyuv
adpcm_g726		libvpx_vp8		png
adpcm_g726le		libvpx_vp9		ppm
adpcm_ima_qt		libwavpack		prores
adpcm_ima_wav		libwebp			prores_aw
adpcm_ms		libwebp_anim		prores_ks
adpcm_swf		libx264			qtrle
adpcm_yamaha		libx264rgb		r10k
alac			libx265			r210
alias_pix		libxavs			ra_144
amv			libxvid			rawvideo
apng			ljpeg			roq
aptx			magicyuv		roq_dpcm
aptx_hd			mjpeg			rv10
ass			mlp			rv20
asv1			movtext			s302m
asv2			mp2			sbc
avrp			mp2fixed		sgi
avui			mpeg1video		snow
ayuv			mpeg2video		sonic
bmp			mpeg4			sonic_ls
cinepak			mpeg4_v4l2m2m		srt
cljr			msmpeg4v2		ssa
comfortnoise		msmpeg4v3		subrip
dca			msvideo1		sunrast
dnxhd			nellymoser		svq1
dpx			opus			targa
dvbsub			pam			text
dvdsub			pbm			tiff
dvvideo			pcm_alaw		truehd
eac3			pcm_f32be		tta
ffv1			pcm_f32le		utvideo
ffvhuff			pcm_f64be		v210
fits			pcm_f64le		v308
flac			pcm_mulaw		v408
flashsv			pcm_s16be		v410
flashsv2		pcm_s16be_planar	vc2
flv			pcm_s16le		vorbis
g723_1			pcm_s16le_planar	vp8_v4l2m2m
gif			pcm_s24be		wavpack
h261			pcm_s24daud		webvtt
h263			pcm_s24le		wmav1
h263_v4l2m2m		pcm_s24le_planar	wmav2
h263p			pcm_s32be		wmv1
h264_v4l2m2m		pcm_s32le		wmv2
huffyuv			pcm_s32le_planar	wrapped_avframe
jpeg2000		pcm_s64be		xbm
jpegls			pcm_s64le		xface
libfdk_aac		pcm_s8			xsub
libgsm			pcm_s8_planar		xwd
libgsm_ms		pcm_u16be		y41p
libilbc			pcm_u16le		yuv4
libmp3lame		pcm_u24be		zlib
libopencore_amrnb	pcm_u24le		zmbv
libopenjpeg

Enabled hwaccels:

Enabled parsers:
aac			dvd_nav			opus
aac_latm		dvdsub			png
ac3			flac			pnm
adx			g729			rv30
av1			gsm			rv40
avs2			h261			sbc
bmp			h263			sipr
cavsvideo		h264			tak
cook			hevc			vc1
dca			mjpeg			vorbis
dirac			mlp			vp3
dnxhd			mpeg4video		vp8
dpx			mpegaudio		vp9
dvaudio			mpegvideo		xma
dvbsub

Enabled demuxers:
aa			ea_cdata		ivf
aac			eac3			ivr
ac3			epaf			jacosub
acm			ffmetadata		jv
act			filmstrip		libmodplug
adf			fits			live_flv
adp			flac			lmlm4
ads			flic			loas
adx			flv			lrc
aea			fourxm			lvf
afc			frm			lxf
aiff			fsb			m4v
aix			g722			matroska
amr			g723_1			mgsts
amrnb			g726			microdvd
amrwb			g726le			mjpeg
anm			g729			mjpeg_2000
apc			gdv			mlp
ape			genh			mlv
apng			gif			mm
aptx			gsm			mmf
aptx_hd			gxf			mov
aqtitle			h261			mp3
asf			h263			mpc
asf_o			h264			mpc8
ass			hevc			mpegps
ast			hls			mpegts
au			hnm			mpegtsraw
avi			ico			mpegvideo
avr			idcin			mpjpeg
avs			idf			mpl2
avs2			iff			mpsub
bethsoftvid		ilbc			msf
bfi			image2			msnwc_tcp
bfstm			image2_alias_pix	mtaf
bink			image2_brender_pix	mtv
bintext			image2pipe		musx
bit			image_bmp_pipe		mv
bmv			image_dds_pipe		mvi
boa			image_dpx_pipe		mxf
brstm			image_exr_pipe		mxg
c93			image_j2k_pipe		nc
caf			image_jpeg_pipe		nistsphere
cavsvideo		image_jpegls_pipe	nsp
cdg			image_pam_pipe		nsv
cdxl			image_pbm_pipe		nut
cine			image_pcx_pipe		nuv
codec2			image_pgm_pipe		ogg
codec2raw		image_pgmyuv_pipe	oma
concat			image_pictor_pipe	paf
data			image_png_pipe		pcm_alaw
daud			image_ppm_pipe		pcm_f32be
dcstr			image_psd_pipe		pcm_f32le
dfa			image_qdraw_pipe	pcm_f64be
dirac			image_sgi_pipe		pcm_f64le
dnxhd			image_sunrast_pipe	pcm_mulaw
dsf			image_svg_pipe		pcm_s16be
dsicin			image_tiff_pipe		pcm_s16le
dss			image_webp_pipe		pcm_s24be
dts			image_xpm_pipe		pcm_s24le
dtshd			image_xwd_pipe		pcm_s32be
dv			ingenient		pcm_s32le
dvbsub			ipmovie			pcm_s8
dvbtxt			ircam			pcm_u16be
dxa			iss			pcm_u16le
ea			iv8			pcm_u24be
pcm_u24le		sdx			v210
pcm_u32be		segafilm		v210x
pcm_u32le		ser			vag
pcm_u8			shorten			vc1
pcm_vidc		siff			vc1t
pjs			sln			vivo
pmp			smacker			vmd
pva			smjpeg			vobsub
pvf			smush			voc
qcp			sol			vpk
r3d			sox			vplayer
rawvideo		spdif			vqf
realtext		srt			w64
redspark		stl			wav
rl2			str			wc3
rm			subviewer		webm_dash_manifest
roq			subviewer1		webvtt
rpl			sup			wsaud
rsd			svag			wsd
rso			swf			wsvqa
rtp			tak			wtv
rtsp			tedcaptions		wv
s337m			thp			wve
sami			threedostr		xa
sap			tiertexseq		xbin
sbc			tmv			xmv
sbg			truehd			xvag
scc			tta			xwma
sdp			tty			yop
sdr2			txd			yuv4mpegpipe
sds			ty

Enabled muxers:
a64			hevc			pcm_s24le
ac3			hls			pcm_s32be
adts			ico			pcm_s32le
adx			ilbc			pcm_s8
aiff			image2			pcm_u16be
amr			image2pipe		pcm_u16le
apng			ipod			pcm_u24be
aptx			ircam			pcm_u24le
aptx_hd			ismv			pcm_u32be
asf			ivf			pcm_u32le
asf_stream		jacosub			pcm_u8
ass			latm			pcm_vidc
ast			lrc			psp
au			m4v			rawvideo
avi			matroska		rm
avm2			matroska_audio		roq
avs2			md5			rso
bit			microdvd		rtp
caf			mjpeg			rtp_mpegts
cavsvideo		mkvtimestamp_v2		rtsp
codec2			mlp			sap
codec2raw		mmf			sbc
crc			mov			scc
dash			mp2			segafilm
data			mp3			segment
daud			mp4			singlejpeg
dirac			mpeg1system		smjpeg
dnxhd			mpeg1vcd		smoothstreaming
dts			mpeg1video		sox
dv			mpeg2dvd		spdif
eac3			mpeg2svcd		spx
f4v			mpeg2video		srt
ffmetadata		mpeg2vob		stream_segment
fifo			mpegts			sup
fifo_test		mpjpeg			swf
filmstrip		mxf			tee
fits			mxf_d10			tg2
flac			mxf_opatom		tgp
flv			null			truehd
framecrc		nut			tta
framehash		oga			uncodedframecrc
framemd5		ogg			vc1
g722			ogv			vc1t
g723_1			oma			voc
g726			opus			w64
g726le			pcm_alaw		wav
gif			pcm_f32be		webm
gsm			pcm_f32le		webm_chunk
gxf			pcm_f64be		webm_dash_manifest
h261			pcm_f64le		webp
h263			pcm_mulaw		webvtt
h264			pcm_s16be		wtv
hash			pcm_s16le		wv
hds			pcm_s24be		yuv4mpegpipe

Enabled protocols:
async			httpproxy		pipe
bluray			icecast			prompeg
cache			librtmp			rtp
concat			librtmpe		srtp
crypto			librtmps		subfile
data			librtmpt		tcp
file			librtmpte		tee
ftp			md5			udp
gopher			mmsh			udplite
hls			mmst			unix
http

Enabled filters:
abench			astats			doubleweave
abitscope		astreamselect		drawbox
acompressor		atadenoise		drawgraph
acontrast		atempo			drawgrid
acopy			atrim			drawtext
acrossfade		avectorscope		drmeter
acrossover		avgblur			dynaudnorm
acrusher		azmq			earwax
acue			bandpass		ebur128
adeclick		bandreject		edgedetect
adeclip			bass			elbg
adelay			bbox			entropy
aderivative		bench			eq
adrawgraph		biquad			equalizer
aecho			bitplanenoise		erosion
aemphasis		blackdetect		extractplanes
aeval			blackframe		extrastereo
aevalsrc		blend			fade
afade			bm3d			fftdnoiz
afftdn			boxblur			fftfilt
afftfilt		bs2b			field
afifo			bwdif			fieldhint
afir			cellauto		fieldmatch
aformat			channelmap		fieldorder
agate			channelsplit		fifo
agraphmonitor		chorus			fillborders
ahistogram		chromahold		find_rect
aiir			chromakey		firequalizer
aintegral		ciescope		flanger
ainterleave		codecview		flite
alimiter		color			floodfill
allpass			colorbalance		format
allrgb			colorchannelmixer	fps
allyuv			colorkey		framepack
aloop			colorlevels		framerate
alphaextract		colormatrix		framestep
alphamerge		colorspace		frei0r
amerge			compand			frei0r_src
ametadata		compensationdelay	fspp
amix			concat			gblur
amovie			convolution		geq
amplify			convolve		gradfun
amultiply		copy			graphmonitor
anequalizer		cover_rect		greyedge
anoisesrc		crop			haas
anull			cropdetect		haldclut
anullsink		crossfeed		haldclutsrc
anullsrc		crystalizer		hdcd
apad			cue			headphone
aperms			curves			hflip
aphasemeter		datascope		highpass
aphaser			dcshift			highshelf
apulsator		dctdnoiz		hilbert
arealtime		deband			histeq
aresample		deblock			histogram
areverse		decimate		hqdn3d
aselect			deconvolve		hqx
asendcmd		deflate			hstack
asetnsamples		deflicker		hue
asetpts			dejudder		hwdownload
asetrate		delogo			hwmap
asettb			deshake			hwupload
ashowinfo		despill			hysteresis
asidedata		detelecine		idet
asplit			dilation		il
ass			displace		inflate
interlace		premultiply		sobel
interleave		prewitt			spectrumsynth
join			pseudocolor		split
kerndeint		psnr			spp
lenscorrection		pullup			sr
life			qp			ssim
limiter			random			stereo3d
loop			readeia608		stereotools
loudnorm		readvitc		stereowiden
lowpass			realtime		streamselect
lowshelf		remap			subtitles
lumakey			removegrain		super2xsai
lut			removelogo		superequalizer
lut1d			repeatfields		surround
lut2			replaygain		swaprect
lut3d			reverse			swapuv
lutrgb			rgbtestsrc		tblend
lutyuv			roberts			telecine
mandelbrot		rotate			testsrc
maskedclamp		sab			testsrc2
maskedmerge		scale			threshold
mcdeint			scale2ref		thumbnail
mcompand		select			tile
mergeplanes		selectivecolor		tinterlace
mestimate		sendcmd			tlut2
metadata		separatefields		tmix
midequalizer		setdar			tonemap
minterpolate		setfield		transpose
mix			setparams		treble
movie			setpts			tremolo
mpdecimate		setrange		trim
mptestsrc		setsar			unpremultiply
negate			settb			unsharp
nlmeans			showcqt			uspp
nnedi			showfreqs		vaguedenoiser
noformat		showinfo		vectorscope
noise			showpalette		vflip
normalize		showspectrum		vfrdet
null			showspectrumpic		vibrance
nullsink		showvolume		vibrato
nullsrc			showwaves		vidstabdetect
oscilloscope		showwavespic		vidstabtransform
overlay			shuffleframes		vignette
owdenoise		shuffleplanes		vmafmotion
pad			sidechaincompress	volume
pal100bars		sidechaingate		volumedetect
pal75bars		sidedata		vstack
palettegen		signalstats		w3fdif
paletteuse		signature		waveform
pan			silencedetect		weave
perms			silenceremove		xbr
perspective		sinc			xstack
phase			sine			yadif
pixdesctest		smartblur		yuvtestsrc
pixscope		smptebars		zmq
pp			smptehdbars		zoompan
pp7

Enabled bsfs:
aac_adtstoasc		h264_redundant_pps	mpeg4_unpack_bframes
av1_metadata		hapqa_extract		noise
chomp			hevc_metadata		null
dca_core		hevc_mp4toannexb	remove_extradata
dump_extradata		imx_dump_header		text2movsub
eac3_core		mjpeg2jpeg		trace_headers
extract_extradata	mjpega_dump_header	vp9_metadata
filter_units		mov2textsub		vp9_raw_reorder
h264_metadata		mp3_header_decompress	vp9_superframe
h264_mp4toannexb	mpeg2_metadata		vp9_superframe_split

Enabled indevs:
fbdev			libcdio			v4l2
iec61883		libdc1394		xcbgrab
lavfi			oss

Enabled outdevs:
caca			oss			xv
fbdev			v4l2
</pre>

[BUILD.md]: https://github.com/mrihtar/sffmpeg/blob/master/BUILD.md
