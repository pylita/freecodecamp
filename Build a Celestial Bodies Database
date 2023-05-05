--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying NOT NULL,
    galaxy_types character varying,
    age_in_millions_of_years numeric,
    has_life boolean,
    description text
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying NOT NULL,
    is_spherical boolean,
    distance_from_planet_km numeric,
    description text,
    planet_id integer
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying NOT NULL,
    planet_types character varying,
    age_in_million_of_years numeric,
    has_life boolean,
    number_of_moons integer,
    distance_from_earth_au numeric,
    description text,
    star_id integer
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet_moon (
    planet_moon_id integer NOT NULL,
    planet_id integer,
    moon_id integer,
    name character varying NOT NULL
);


ALTER TABLE public.planet_moon OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying NOT NULL,
    star_types character varying,
    age_in_million_of_years numeric,
    number_of_planets integer,
    description text,
    galaxy_id integer
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (2, 'Black Eye Galaxy', 'spiral galaxy', NULL, NULL, NULL);
INSERT INTO public.galaxy VALUES (3, 'Cigar Galaxy', 'irregular galaxy', NULL, NULL, NULL);
INSERT INTO public.galaxy VALUES (4, 'Small Magellanic Cloud', 'irregular galaxy', NULL, NULL, NULL);
INSERT INTO public.galaxy VALUES (5, 'Milky Way', 'spiral galaxy', NULL, NULL, NULL);
INSERT INTO public.galaxy VALUES (6, 'Needle Galaxy', 'spiral galaxy', NULL, NULL, NULL);
INSERT INTO public.galaxy VALUES (7, 'Messier 49', 'elliptical galaxy', NULL, NULL, NULL);
INSERT INTO public.galaxy VALUES (1, 'Andromeda Galaxy', 'spiral galaxy', NULL, NULL, NULL);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (2, 'Ganymede', true, 1070400, NULL, 5);
INSERT INTO public.moon VALUES (1, 'Moon', true, 384400, NULL, 3);
INSERT INTO public.moon VALUES (3, 'Titan', true, 1200000, NULL, 6);
INSERT INTO public.moon VALUES (4, 'Enceladus', true, 238000, NULL, 6);
INSERT INTO public.moon VALUES (5, 'Epimetheus', false, 151000, NULL, 6);
INSERT INTO public.moon VALUES (6, 'Dione', true, 377400, NULL, 6);
INSERT INTO public.moon VALUES (7, 'Helene', false, 377400, NULL, 6);
INSERT INTO public.moon VALUES (8, 'Hyperion', false, 1500000, NULL, 6);
INSERT INTO public.moon VALUES (9, 'Janus', false, 151000, NULL, 6);
INSERT INTO public.moon VALUES (10, 'Methone', false, 194000, NULL, 6);
INSERT INTO public.moon VALUES (11, 'Io', true, 422000, NULL, 5);
INSERT INTO public.moon VALUES (12, 'Europa', true, 671000, NULL, 5);
INSERT INTO public.moon VALUES (13, 'Callisto', true, 1883000, NULL, 5);
INSERT INTO public.moon VALUES (14, 'Phobos', false, 9234, NULL, 4);
INSERT INTO public.moon VALUES (15, 'Deimos', false, 23455, NULL, 4);
INSERT INTO public.moon VALUES (16, 'Ariel', true, 190900, NULL, 7);
INSERT INTO public.moon VALUES (17, 'Oberon', true, 583520, NULL, 7);
INSERT INTO public.moon VALUES (18, 'Puck', false, 150, NULL, 7);
INSERT INTO public.moon VALUES (19, 'Naiad', false, 48224, NULL, 8);
INSERT INTO public.moon VALUES (20, 'Triton', true, 354759, NULL, 8);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (2, 'Venus', 'terrestrial planet', 4503, false, 0, 0.28, NULL, NULL);
INSERT INTO public.planet VALUES (1, 'Mercury', 'terrestrial planet', 4503, false, 0, 0.56, NULL, NULL);
INSERT INTO public.planet VALUES (3, 'Earth', 'terrestrial planet', 4543, true, 1, NULL, NULL, NULL);
INSERT INTO public.planet VALUES (4, 'Mars', 'terrestrial planet', 4603, false, 2, 1.76, NULL, NULL);
INSERT INTO public.planet VALUES (5, 'Jupiter', 'gas giant', 4603, false, 95, 5.92, NULL, NULL);
INSERT INTO public.planet VALUES (6, 'Saturn', 'gas giant', 4503, false, 83, 10.16, NULL, NULL);
INSERT INTO public.planet VALUES (7, 'Uranus', 'neptunian', 4503, false, 27, 20.65, NULL, NULL);
INSERT INTO public.planet VALUES (8, 'Neptune', 'neptunian', 4503, false, 14, 29.09, NULL, NULL);
INSERT INTO public.planet VALUES (9, 'Kepler-186f', 'terrestrial planet', 4000, false, NULL, 35269549, NULL, NULL);
INSERT INTO public.planet VALUES (10, 'HD 209458 b', 'gas giant', 4000, false, NULL, 10060000, NULL, NULL);
INSERT INTO public.planet VALUES (11, 'Kepler-16b', 'gas giant', 2000, false, NULL, 12650000, NULL, NULL);
INSERT INTO public.planet VALUES (12, 'Kepler-22b', 'super earth', 4000, false, NULL, 40160000, NULL, NULL);


--
-- Data for Name: planet_moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet_moon VALUES (1, 5, 2, 'Ganymede');
INSERT INTO public.planet_moon VALUES (2, 3, 1, 'Moon');
INSERT INTO public.planet_moon VALUES (3, 6, 3, 'Titan');
INSERT INTO public.planet_moon VALUES (4, 6, 4, 'Enceladus');


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Rigel', 'B8Ia', 8, 14, NULL, NULL);
INSERT INTO public.star VALUES (2, 'Sirius A', 'A0mA1 Va', 242, NULL, NULL, NULL);
INSERT INTO public.star VALUES (3, 'Alpheratz', 'B8IVpMnHg', 60, NULL, NULL, NULL);
INSERT INTO public.star VALUES (4, 'Sun', 'G2V', 4500, 8, NULL, NULL);
INSERT INTO public.star VALUES (5, 'Arcturus', 'K1.5 III Fe−0.5', 7100, NULL, NULL, NULL);
INSERT INTO public.star VALUES (6, 'Vega', 'A0Va', 455, 1, NULL, NULL);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 7, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--
SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 12, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 6, true);


--
-- Name: galaxy galaxy_galaxy_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_galaxy_id_key UNIQUE (galaxy_id);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_moon_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_moon_id_key UNIQUE (moon_id);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet_moon planet_moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_moon
    ADD CONSTRAINT planet_moon_pkey PRIMARY KEY (planet_moon_id);


--
-- Name: planet_moon planet_moon_planet_moon_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_moon
    ADD CONSTRAINT planet_moon_planet_moon_id_key UNIQUE (planet_moon_id);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: planet planet_planet_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_planet_id_key UNIQUE (planet_id);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);

--
-- Name: star star_star_id_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_star_id_key UNIQUE (star_id);


--
-- Name: planet_moon planet_moon_moon_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_moon
    ADD CONSTRAINT planet_moon_moon_id_fkey FOREIGN KEY (moon_id) REFERENCES public.moon(moon_id);


--
-- Name: planet_moon planet_moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_moon
    ADD CONSTRAINT planet_moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);

--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

