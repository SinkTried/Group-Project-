-- phpMyAdmin SQL Dump
-- version 5.2.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Nov 12, 2025 at 02:37 AM
-- Server version: 10.4.32-MariaDB
-- PHP Version: 8.2.12

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `appointments`
--

-- --------------------------------------------------------

--
-- Table structure for table `appntmnt`
--

CREATE TABLE `appntmnt` (
  `appntmnt_id` int(11) NOT NULL,
  `doc_id` int(11) DEFAULT NULL,
  `full_name` varchar(255) NOT NULL,
  `dob` date DEFAULT NULL,
  `pin_hash` varchar(255) NOT NULL,
  `day_selected` varchar(20) DEFAULT NULL,
  `time_selected` varchar(50) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `appntmnt`
--

INSERT INTO `appntmnt` (`appntmnt_id`, `doc_id`, `full_name`, `dob`, `pin_hash`, `day_selected`, `time_selected`) VALUES
(3, 1, 'John Doe', '1999-01-01', '$2y$10$6XiTfwWrSTk5.dXjBKM4XeQEZJ1uz11ZtQzQNMuTjZd9mGTsXl.cC', 'Monday', '09:00 AM - 10:00 AM');

-- --------------------------------------------------------

--
-- Table structure for table `doctor`
--

CREATE TABLE `doctor` (
  `doc_id` int(11) NOT NULL,
  `name` varchar(255) NOT NULL,
  `specialty` varchar(255) NOT NULL,
  `days_available` set('Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday') DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `doctor`
--

INSERT INTO `doctor` (`doc_id`, `name`, `specialty`, `days_available`) VALUES
(1, 'Dr. Alice Smith', 'Cardiology', 'Monday,Wednesday,Friday'),
(2, 'Dr. Bob Johnson', 'Pediatrics', 'Tuesday,Thursday');

-- --------------------------------------------------------

--
-- Table structure for table `patients`
--

CREATE TABLE `patients` (
  `pid` int(11) NOT NULL,
  `name` varchar(200) NOT NULL,
  `pin` int(4) NOT NULL,
  `dob` date NOT NULL,
  `age` tinyint(4) GENERATED ALWAYS AS (timestampdiff(YEAR,`dob`,curdate())) VIRTUAL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

--
-- Dumping data for table `patients`
--

INSERT INTO `patients` (`pid`, `name`, `pin`, `dob`) VALUES
(1, 'John Smith', 5566, '1980-03-12');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `appntmnt`
--
ALTER TABLE `appntmnt`
  ADD PRIMARY KEY (`appntmnt_id`),
  ADD KEY `doc_id` (`doc_id`);

--
-- Indexes for table `doctor`
--
ALTER TABLE `doctor`
  ADD PRIMARY KEY (`doc_id`);

--
-- Indexes for table `patients`
--
ALTER TABLE `patients`
  ADD PRIMARY KEY (`pid`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `appntmnt`
--
ALTER TABLE `appntmnt`
  MODIFY `appntmnt_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;

--
-- AUTO_INCREMENT for table `doctor`
--
ALTER TABLE `doctor`
  MODIFY `doc_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `patients`
--
ALTER TABLE `patients`
  MODIFY `pid` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- Constraints for dumped tables
--

--
-- Constraints for table `appntmnt`
--
ALTER TABLE `appntmnt`
  ADD CONSTRAINT `appntmnt_ibfk_1` FOREIGN KEY (`doc_id`) REFERENCES `doctor` (`doc_id`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
